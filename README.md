# 简介

<img src="https://i.loli.net/2020/04/22/Hy7kwJL8FDr6I5O.png" width = "360" height = "640" alt="图片名称" align=center />

这是一个在Android上向[废话胶囊（b言b语）](https://github.com/daibor/nonsense.fun)发送内容的简单 Tasker 工程。

https://sspai.com/post/60024

图文教程请见 [我的博客](https://jimlee2002.github.io/posts/4394c3fa.html)。

**本工程未在非root环境上测试，可能需要root权限才能使用。**

# 安装配置

## 1. 直接下载安装已经导出好的[apk文件](https://github.com/jimlee2002/nonsense.fun_tasker/releases)

该应用使用插件`Tasker App Factory`导出。

注意，使用该应用**需要root权限**。

## 2. 导入Tasker工程

**注意：部分手机可能需要Root权限才能使用，该工程默认开启``使用Root运行``，可以自行到`场景/Main/发送/按下` 的第6个和第8个任务里关掉。**

1. [下载](https://github.com/jimlee2002/nonsense.fun_tasker/releases)``bb.prj.xml``，存入到手机任意你找得到的位置。

2. 下载安装Tasker。

3. 进入主界面长按左下角的按钮，点击`导入项目`，在打开的界面中找到并打开刚才存入的`bb.prj.xml。`

   > 提示：点击右下角的手机按钮可以快速回到内部储存空间目录
   >
   
4. 完成后回到主界面，点击应用栏里图标长得和Tasker很像的`Tasker Secondary`，打开界面。

5. **长按**发送按钮，打开设置页面进行必要设置。

   **Title：** 这里是发送界面顶端的文字，请随意修改。

   **AppID、MasterKey：** 网页打开LeanCloud，在你的项目里点击``设置/应用Keys``，复制对应的密钥分别填入。

   **className：** 一般是`content`，只要你是按照[少数派的指南](https://sspai.com/post/60024)来做的话。

   **--insecure：** 是否在脚本命令末尾加上`--insecure`参数。默认关闭，如果无法发送可以尝试打开这个选项试试。
   
   **完成后点击确认返回**。

这样就配置完成了，请试试看吧！

## 3. Leancloud 国际版 API 绑定域名

LeanCloud 国际版共享域名于 2022 年 8 月 1 日起不再向中国大陆的最终用户提供服务，如果应用的用户主体是在中国大陆，使用数据存储、即时通信、推送与短信服务的用户，需要在控制台绑定 API 自定义域名；使用云引擎服务的用户，需要在控制台绑定云引擎自定义域名。

自行到`场景/Main/发送/按下`，手动替换这两处 Shell 命令的 %reqURL 为你的域名就好：

<img src="https://s2.loli.net/2022/08/04/bBlPjizF5KETa4G.png" width = "360" height = "640" alt="图片名称" align=center /> <img src="https://s2.loli.net/2022/08/04/waJSrPtqg48FkXh.png" width = "360" height = "640" alt="图片名称" align=center />

如果还是不行，可以尝试：

打开发送界面，**长按**发送按钮，打开设置页面调整`--insecure`参数。

   **--insecure：** 是否在脚本命令末尾加上`--insecure`参数。默认关闭，如果无法发送可以尝试打开这个选项试试。

# Tasker工程使用方法

## 通过 Tasker Secondary 打开

## 通过桌面小工具创建快捷方式打开

1. 打开Tasker，然后**点击返回键**回到主界面。

2. 在桌面上新建Tasker的桌面小部件"任务"，

   进入界面后选择`Show UI，

   在界面下方选择图标，然后点击左上角返回桌面，

   完成。

## 自行导出为APK安装

**注意：你必须拥有手机的Root权限，并勾选`场景/Main/发送/按下`。的第6个和第8个任务中的`使用Root运行`选项 。**

1. Gogle Play安装`Tasker App Factory`。

2. 打开Tasker，主界面左下方长按选择已经导入的项目,选择`导出\作为应用`。

   >  提示：你可以通过点击`更名`重命名工程名称来修改应用名。

3. 根据提示输入包名和版本号。

4. 点击左上角返回，Tasker会将项目以APK格式导出到``内部储存/Tasker/factory/kids``并安装。

# 后记

界面如果有问题可以自行在Tasker的`场景`中修改。

个人能力有限，做的比较粗糙，还请不吝赐教！

# 致谢

感谢 [daibor](https://github.com/daibor) 制作了这么棒的[项目](https://github.com/daibor/nonsense.fun)。

感谢少数派的 @SoSo 在评论下分享的方法启发了这个工程。

# ToDo
- [x] 平板适配
- [ ] 多人版适配
