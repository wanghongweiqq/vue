Ruby2445
 
Ruby，一种简单快捷的面向对象（面向对象程序设计）脚本语言，Ruby明显比其他类似的编程语言（如Perl或Python）年轻，Ruby归根结底源于Perl和Lisp两类语言，与C，C++，C#，java是不同大类。

Ruby的变量有一定的规则，以$开头的一定是全局变量，以@开头的都是实例变量，而以@@开头的是类变量。常数则以大写字母开头；这种方法，对文本编辑器的命令补全很有帮助，如在vim下先键入$及开头字母，再敲击Ctrl+p，则可专门补全本文件以及关联文件中的全局变量，perl与php亦有此优点。
已经定义的类可以在运行时修改

语言特点
•	Ruby 是开源的，在Web 上免费提供，但需要一个许可证。[5] 
•	Ruby 是一种通用的、解释的编程语言。
•	Ruby 是一种真正的面向对象编程语言。
•	Ruby 是一种类似于 Python 和 Perl 的服务器端脚本语言。
•	Ruby 可以用来编写通用网关接口（CGI）脚本。
•	Ruby 可以被嵌入到超文本标记语言（HTML）。
•	Ruby 语法简单，这使得新的开发人员能够快速轻松地学习 Ruby。
•	Ruby 与 C++ 和 Perl 等许多编程语言有着类似的语法。
•	Ruby 可扩展性强，用 Ruby 编写的大程序易于维护。
•	Ruby 可用于开发的 Internet 和 Intranet 应用程序。
•	Ruby 可以安装在 Windows 和 POSIX 环境中。
•	Ruby 支持许多 GUI 工具，比如 Tcl/Tk、GTK 和 OpenGL。
•	Ruby 可以很容易地连接到 DB2、MySQL、Oracle 和 Sybase。
•	Ruby 有丰富的内置函数，可以直接在 Ruby 脚本中使用。[5]


Compass

Compass是什么？

简单说，Compass是Sass的工具库（toolkit）。
Sass本身只是一个编译器，Compass在它的基础上，封装了一系列有用的模块和模板，补充Sass的功能。它们之间的关系，有点像Javascript和jQuery、Ruby和Rails、python和Django的关系。

安装
Compass是用Ruby语言开发的，所以安装它之前，必须安装Ruby。

假定你的机器（Linux或OS X）已经安装好Ruby，那么在命令行模式下键入：
sudo gem install compass
如果你用的是Windows系统，那么要省略前面的sudo。

编译
在写代码之前，我们还要知道如何编译。因为我们写出来的是后缀名为scss的文件，只有编译成css文件，才能用在网站上。

Compass的编译命令是
　　compass compile
该命令在项目根目录下运行，会将sass子目录中的scss文件，编译成css文件，保存在stylesheets子目录中。

默认状态下，编译出来的css文件带有大量的注释。但是，生产环境需要压缩后的css文件，这时要使用--output-style参数。
　　compass compile --output-style compressed

Compass只编译发生变动的文件，如果你要重新编译未变动的文件，需要使用--force参数。
　　compass compile --force

除了使用命令行参数，还可以在配置文件config.rb中指定编译模式。
　　output_style = :expanded
:expanded模式表示编译后保留原格式，其他值还包括:nested、:compact和:compressed。进入生产阶段后，就要改为:compressed模式。
　　output_style = :compressed

也可以通过指定environment的值（:production或者:development），智能判断编译模式。
　　environment = :development
　　output_style = (environment == :production) ? :compressed : :expanded

在命令行模式下，除了一次性编译命令，compass还有自动编译命令
　　compass watch
运行该命令后，只要scss文件发生变化，就会被自动编译成css文件。


http://www.ruanyifeng.com/blog/2012/11/compass.html
