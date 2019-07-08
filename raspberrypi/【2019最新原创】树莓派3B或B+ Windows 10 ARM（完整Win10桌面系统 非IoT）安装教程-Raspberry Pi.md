# 【2019最新原创】树莓派3B/B+ Windows 10 ARM（完整Win10桌面系统 非IoT）安装教程-Raspberry Pi
~~## 原标题：树莓派3B+ windows10ARM SD卡完美2分钟启动镜像*~~ ***
现全新改为教程帖
目前发帖时间在19年2月以前的教程基本已经失效或安装成功后非常不稳定，本教程无需手动输入一条命令，无需dg，完全图形化部署且系统可稳定运行。
之前因为个人项目需要win环境，在树莓派上装windows10ARM（非IOT）大概花了我4天时间。。期间遇到各种坑，重新部署N遍镜像后终于成功，现发个博客记录一下。
现存问题及可行性分析：
树莓派性能上比不过pc的。USB、有线网卡、声卡、GPIO等已完美驱~~原标题：树莓派3B+ windows10ARM SD卡完美2分钟启动镜像~~
现全新改为教程帖
目前发帖时间在19年2月以前的教程基本已经失效或安装成功后非常不稳定，本教程无需手动输入一条命令，无需dg，完全图形化部署且系统可稳定运行。
之前因为个人项目需要win环境，在树莓派上装windows10ARM（非IOT）大概花了我4天时间。。期间遇到各种坑，重新部署N遍镜像后终于成功，现发个博客记录一下。
现存问题及可行性分析：
树莓派性能上比不过pc的。USB、有线网卡、声卡、GPIO等已完美驱动，正常使用无死机问题。目前显卡全球无解，界面效果会比较卡顿，不播放视频影响不大。wifi、蓝牙同样全球无解！所以不推荐要把它当作主力pc用。SD卡容量最低16GB，最好使用4k读写速度快一些的卡。
运行截图如下
![20190519184151691.jpg][1]
![20190519183954882.png][2]
**下面正式开始安装**
资源下载链接
（2019.5更新）[https://download.csdn.net/download/weixin_42753993/11188084][3]
（2019.6更新）[https://download.csdn.net/download/weixin_42753993/11255272][4]
更新了windows arm1803镜像的下载方式（**推荐**）

一.下载windows10 ARM镜像：
将提供的.cmd脚本放到一个剩余空间比较充足的分区中（最好>50G）
关掉杀毒软件（防止误杀进程，放心没病毒）
双击运行脚本
接着：静坐/喝茶/小憩

（2小时后）

二.开始安装
将你的SD卡插入电脑，并格式化之
挂载第一步生成的.iso镜像文件（方法自行百度或双击**.iso文件**）
双击运行Installer.Raspberry.Application.exe（如杀毒软件误报，请添加信任）
软件运行环境：win10&NET Framework 4.6.1
注意：本教程的安装程序提供的是官方老版本（已绝版），无需fq下载资源包即可离线使用
如需新版本请自行更新（使用老版本没有任何问题，安装效果与新版本无异）
这个界面仔细阅读后点 OK
![20190519193737735.png][5]
来到主程序界面了
![20190519193809774.png][6]
首先点击“Advanced”
点击中间的“import core package”按钮，将下载好的core package导入进去（不要解压缩）
![20190519193902103.png][7]
接着点击Advance左边的按钮返回主界面

软件里选择你的SD卡（**千万看清楚了**）
点击“Browse”，将镜像sources文件夹下的“install.wim”文件选中
![20190519185947103.png][8]
下方软件会显示版本等信息。
完成之后如下图：
![2019051919400915.png][9]
你会发现Deploy按钮可以点击了。检查下安装的sd卡有没有选错，可以按下它了。
到此你已经完成一多半
耐心等待1-3小时，等待它完成。

================================================================
三.部署系统
将SD卡拔下来插到树莓派上，接上**有线**鼠标键盘，最好插上网线，上电！
大大的树莓派标识出来了。
![2019051919294850.jpg][10]
别着急，不设置会直接进shell的。
按esc，会进入一个类似电脑bios的配置界面，like this
![20190519192922681.jpg][11]
（键盘）选择Device Manager==>Raspberry Pi Configuration==>Chipset Configuration==>把cpu clock改为max，usd routing改为 Arasan SDHCI。保存重启
![20190519193019928.jpg][12]
**6月5日更新：这里之前的文章写错了，感谢 昵称“汽车明明”的提醒。**
再次按esc进入配置界面，选择第三个Boot Maintenance Manager =>Boot Options=>Change Boot Order
进入后回车，按键盘+号将SD/MMC on xxx那一项移到最上边，保存重启
![20190605181651515.jpg][13]
![20190605181706532.jpg][14]
熟（可）悉（爱）的win10图标出来了！
![20190519193056107.jpg][15]
之后等待约1小时，会出来和普通pc安装win10一样的设置界面，设置完成后就进入桌面了
这里如果遇到黄字“oobe xxxxx”这样的错误，务必要有耐心。不要点跳过，更不要放弃。点击重试，可能需要重试4、5次甚至更多，再不行就点击左上角返回按钮到上一步重来一遍 肯定会通过的
但千万不要跳过。
千万不要跳过。
千万不要跳过。
重要的事情说三遍

========================================================
教程结束
如果在安装过程中遇到任何问题，欢迎在下方留言讨论。

作者：01studio 
来源：CSDN 
原文：https://blog.csdn.net/weixin_42753993/article/details/88214838 
版权声明：本文为博主原创文章，转载请附上博文链接！


  [1]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/4098585444.jpg
  [2]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/2047773950.png
  [3]: https://download.csdn.net/download/weixin_42753993/11188084
  [4]: https://download.csdn.net/download/weixin_42753993/11255272
  [5]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/1139998420.png
  [6]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/520047163.png
  [7]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/937919790.png
  [8]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/1582784436.png
  [9]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/1127839944.png
  [10]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/2585289656.jpg
  [11]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/399101150.jpg
  [12]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/601169904.jpg
  [13]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/3909513108.jpg
  [14]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/3588584168.jpg
  [15]: https://github.com/hmsjy2017/data-backup/blob/master/raspberrypi/pictures/3332266120.jpg
  
