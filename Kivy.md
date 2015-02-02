

Kivy是一套专门用于跨平台快速应用开发的开源框架，使用Python和Cython编写，基于OpenGL ES 2，其核心开发成员主要包括：Mathieu Virbel、Thomas Hansen、Gabriel Pettier等。Kivy对于多点触控有着非常良好的支持，不仅能让开发者快速完成简洁的交互原型设计，还支持代码重用和部署，无论是为Windows、OS X、Linux还是Android和iOS，开发者都可以使用相同的代码库。


主要特性：

    跨平台：只需一套代码，即可运行于主流桌面和移动平台之上，支持大部分原生输入协议和设备，包括WM_Touch、WM_Pen、Mac OS X Trackpad和Magic Mouse、Mtdev、Linux Kernel HID、TUIO，此外，还包含一个多点触控的鼠标模拟器。
    开源免费：一直以来，Kivy都是100%供开发者免费使用的，从1.7.2版开始基于MIT许可协议开源，而在此之前，则遵循LGPL3许可证。
    拥有丰富的API文档和开发指南。
    GPU加速：通过OpenGL ES 2实现硬件加速，使用了现代化、快速的图形通道。工具集本身拥有超过20个小工具，具有高度的可扩展性，大部分使用Cython编写，并通过回归测试。

Kivy从最初的1.0到1.8.0版本，发展已超过三年，并且，其开发团队仍然在不断地更新和优化中。使用Kivy不仅易于使用，更通过模板技术降低了后续代码的维护难度，许多开发者评价其为颇让人惊艳的一款NUI框架。

在2048风靡之时，Mathieu Virbel用Kivy小试牛刀地开发了一款Kivy版的2048，绝对可以充当开发者学习Kivy的Hello World：

[py] view plaincopy在CODE上查看代码片派生到我的代码片

    #when the setup is done and it start working, it is easy to login  
    PythonActivity = autoclass('org.renpy.android.PythonActivity')  
     GameHelper = autoclass('com.google.example.games.basegameutils.GameHelper')  
     gh_instance = GameHelper(PythonActivity.mActivity, GameHelper.CLIENT_ALL)  
     gh_instance_listener = GameHelperListener()  
     gh_instance.setup(gh_instance_listener)  
     gh_instance.onStart(PythonActivity.mActivity)  
     android.activity.unbind(on_activity_result=_on_activity_result)  
     android.activity.bind(on_activity_result=_on_activity_result)  

[py] view plaincopy在CODE上查看代码片派生到我的代码片

    #that's how you can unlock achievement  
    #uid is the Google UID for the achievement you want  
    if gh_instance.isSignedIn():  
        Games.Achievements.unlock(gh_instance.getApiClient(), uid)  

[py] view plaincopy在CODE上查看代码片派生到我的代码片

    #put the user score on the leaderboard  
    #uid is the Google UID for the leaderboard you've created.  
    #You can have multiple leaderboard.  
    if gh_instance.isSignedIn():  
        Games.Leaderboards.submitScore(gh_instance.getApiClient(), uid, score)  

现在，您还可以进入Kivy的mobilehub主页进行资源分享和讨论。开发者可直接登陆Github下载Kivy，想要了解更多关于Kivy框架的信息及其开发指南，可查看Kivy官网。

本文为CSDN原创文章，未经允许不得转载，如需转载请联系market#csdn.net(#换成@)

顶
    11

踩
    0

推荐阅读相关主题： 应用 linux kernel 移动平台 开源框架 硬件加速 开发者

    相关文章
    最新报道

    ChocolateChip-UI：能“逆转”的跨平台应用开发框架
    详解Visual Studio Emulator for Android，微软的Mobile First！
    跨平台2D/3D游戏开发框架libGDX发布1.2.0更新
    Ratchet：构建移动应用原型，新版支持Android
    移动UI框架Fries：私人定制最Sexy的用户界面
    Framer：开源原型设计工具，巨头们的心头好

已有18条评论
还可以再输入500个字

