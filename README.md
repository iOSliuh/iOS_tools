# iOS_tools
some tools used usually in iOS development


一、依赖管理工具：CocoaPods
       CocoaPods已成为iOS开发事实上的依赖管理标准工具，可以大大节省设置和更新第三方开源库的时间。
       使用：
       集成CocoaPods后，在项目根目录创建Podfile文件，将第三方开源库依次以例如pod 'Reachability',  '~> 3.1.0'格式列在Podfile文件中，然后执行pod install，CocoaPods即可自动将相应第三方开源库源代码下载至工程中，且为工程设置好相应的系统依赖和编译参数。每次更改了Podfile文件后，需要重新执行一次pod update命令。
        原理：
        CocoaPods将所有的依赖库放到另一个名为Pods的项目中，然后让主项目依赖Pods项目，如此，源码管理工作从主项目转移到了Pods项目。

二、API接口测试工具：Postman
       Postman是一种网页调试与发送网页http请求工具，可方便地用于API测试。
       优点：
       支持各种请求类型: get、post、put、patch、delete 等
       支持在线存储数据，通过账号可进行迁移数据
       支持请求 header 和请求参数的设置
       支持不同认证机制，包括 Basic Auth，Digest Auth，OAuth 1.0，OAuth 2.0 等
       响应数据自动按照语法格式高亮，包括 HTML，JSON 和 XML

三、网络封包分析工具：Charles
       可从Charles官网http://www.charlesproxy.com下载安装Charles。
       原理：
         Charles通过将自己设置成系统的网络访问代理服务器，使得所有的网络访问请求都通过它来完成，从而实现网络封包的截取和分析。
       功能：
         1、支持SSL代理。
         2、支持流量控制。可模拟慢速网络及等待时间较长的请求。
         3、支持AJAX调试。可自动将JSON活XML数据格式化，以便查看。
         4、支持重发网络请求、支持修改网络请求参数和响应参数。
         5、支持网络请求的截获和动态修改。

四、App图片资源压制工具：App Icon Gear
        App Icon Gear是App图标、启动图及Xcode Asset图片压制工具，可以非常方便地与Xcode协同工作，操作简单快速压制各种尺寸的图片。

五、移动统计工具：Flurry（另有同类工具友盟）
        Flurry为移动应用提供数据统计和分析功能。可从官网http://www.flurry.com创建应用并下载SDK进行集成。
        Flurry能够统计出应用的使用情况，包括每天/周/日登陆用户、新用户、活跃用户数、应用使用次数及用户地区及移动设备版本、型号等信息。除此之外还可以通过提供的API进行针对性的统计。如统计某个按钮的点击、某个页面的停留时间等。另外，还可统计Crash情况。
      
六、崩溃日志记录工具：Crashlytics（另有Bugly）
       Crashlytics,专门为移动应用保存和分析应用崩溃信息的专业工具。可以全面记录崩溃信息且便于管理崩溃日志，分门别类且自动设置优先级。
      可在官网http://try.crashlytics.com申请账号、创建应用并下载集成SDK。
      平常也经常用到腾讯Bugly进行崩溃管理。

七、App Store统计工具：App Annie（另有苹果App Store Connect）
       App Annie是App Store数据的统计分析工具，可统计App在App Store的下载量、排名变化、销售收入及用户评价等信息。
       使用App Annie需要在iTunes connect中配置一个Sales类型账号，控制权限。然后可在官网http://www.appannie.com/ 上注册账号及配置相关信息。
      另外，平常也经常使用苹果官方出品的App Store Connect进行App Store数据统计，也较好用。

八、Xcode插件
       Xcode插件管理工具Alcatraz，它能管理Xcode插件、模板及颜色配置。可以直接集成到Xcode的图形界面，就仿佛在使用Xcode自带的功能一样。
命令行安装Alcatraz:
       mkdir -p ~/Library/Application\ Support/Developer/Shared/Xcode/Plug-ins;
       curl -L http://git.io/10QWeA | tar xvx -C ~/Library/Application\ Support/Developer/Shared/Xcode/Plug-ins。
安装成功后重启Xcode，就可在Xcode顶部菜单中找到Alcatraz: Window--Package Manager。
可在插件列表页面搜索及安装所需插件。

       常用Xcode插件：
       1、KSImageNamed，可帮助输入[UIImage imageNamed:]中的资源名的插件。当输入[UIImage imageNamed:]时，会自动弹出上下文菜单，共你选择所需图片资源名字，且在选择图片资源时可在左侧预览该资源。
       2、Xvim，可在Xcode的编辑窗口中开启vim模式，其最大好处是可以全键盘操作，方便移动光标以及复制、粘贴代码。XVim对Xcode的分栏模式也有很好的支持，可用快捷键Ctrl + W切换当前编辑的分栏。
       3、FuzzyAutocompletePlugin,可使用模糊的方式来进行代码自动补全。如需要重载viewDidAppear:方法，可以键入vda(view、did、appear三个单词的首字母)，或任意符合viewDidAppear整个单词出现顺序的子串（如vdapp,idear等），即可匹配到该方法。
       4、XToDo,可查找项目中所有的带有TODO、FIXME、???、!!!标记的注释。XToDo提供一个汇总的界面，集中显示所有的未完成的TODO和FIXME标记。
       5、SCXcodeSwitchExpander,可迅速在switch语句中填充枚举类型的每种可能的取值。
       6、VVDocumenter，可自动生成代码注释，可以方便地将函数的参数名和返回值提取出来，结合appledoc命令，就可方便地输出帮助文档。
        7、CLangFormat，自动调整代码风格的工具。可以更好的对代码进行重新排版，且内置了各种排版风格，也支持自定义风格。
       8、ColorSense，UIColor颜色输入辅助工具，可帮助在编写UIColor代码时，实时预览对应颜色。

九、其他工具
1、数码取色器（DigitalColor Meter）（Mac实用工具内自带），类似的还有xScope。
2、ImageOptim,图像压缩工具。ImageOptim使用各种开源的图像压缩工具，然后去效果最好的一个。可从官网http://imageoptim.com/下载安装。
3、马克鳗，可方便地在美术设计稿上标注相应界面元素的大小、颜色、边距、说明等。http://www.getmarkman.com/。
4、Dash，一款API文档查询及代码片段管理工具。蒲公英，类似苹果TestFlight的内测分发工具。
 5、xctool，是Facebook开源的一个iOS编译和测试工具，纯命令行工具。可以使用xctool在命令行下进行编译和单元测试，然后将测试结果集成到Jenkins中，这样实现了自动化的持续集成。安装：brew install xctool。
6、appledoc,从源代码中抽取文档的工具，可从iOS工程的源代码中抽取相应的注释，生成帮助文档。安装：brew install appledoc。


