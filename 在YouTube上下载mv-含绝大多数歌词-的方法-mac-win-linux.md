# 在YouTube上下载mv**（含绝大多数歌词）**的方法(mac/win/linux)

------



| 更新信息        |                |
| ----------- | -------------- |
| 2017.7.12更新 | **修正了文章的内容错误** |

------



<u>＊YouTube在国内早已被封，需要挂**代理**，方法这我就不多说了＊</u>

使用软件clipgrab+Musixmatch Lyrics for YouTube+google2srt+mkvtoolnix(可选，封装歌词用)。

- ## 第一步 *下载MV(视频文件)*

  使用软件[clipgrab](https://clipgrab.org)（当然也可以使用其他软件如youtube-dl）

  1. ### clipgrab的介绍

     clipgrab是一个非常不错的下载YouTube视频的软件，虽然不支持列表下载，但界面友好且支持代理，可下载8k视频，没有广告和捆绑软件。力荐！

     截图如下

     官网下载截图![f0bad2475733a409.jpg](https://ooo.0o0.ooo/2017/01/31/5890b08512d25.jpg)

     软件截图（代理部分）

     ![40507b6ef9dadab9.jpg](https://ooo.0o0.ooo/2017/01/31/5890b0fb37a9d.jpg)

  2. ### clipgrab的使用

     找一个YouTube的视频比如[https://www.youtube.com/watch?v=c6rP-YP4c5I](https://www.youtube.com/watch?v=c6rP-YP4c5I)，粘贴在地址栏里（Mac版的复制链接后将自动粘贴到地址栏里，其他系统自测），选择想要的分辨率或格式点击“获取这个视频”后选择保存位置即可，如图![f5e63676cf223eaa.jpg](https://ooo.0o0.ooo/2017/02/01/5891a442dc6f1.jpg)

     ⚠️注意：Linux系统需要安装ffmpeg，否则格式分辨率功能将不完整

- ## 第二步 *下载歌词*（需要chrome浏览器）

  YouTube上的歌词的有无是上传者是否上传决定的。大多mv一般都不含歌词，可使用chrome上的一个拓展软件[Musixmatch Lyrics for YouTube](https://chrome.google.com/webstore/detail/musixmatch-lyrics-for-you/gfenjblodoldnbiddmggcbkcapiolbig) 这个软件的公司是个专注于歌词的公司，数据库里有绝大多数YouTube mv的歌词，可以使用它来获取歌词

  1. 下载并安装Musixmatch Lyrics for YouTube（点击链接安装即可，过程省略）

  2. 使用开发者工具获取歌词（xml文件）

     打开视频后在空白处点击检查（windows下可按f12快捷键）

     如图![3d0e153d3e4f4106.jpg](https://ooo.0o0.ooo/2017/01/31/5890b10732106.jpg)

     最上面选择network后找name下?res或timetext开头的文件即为歌词

     如图（timetext）![54c21475795311e0.jpg](https://ooo.0o0.ooo/2017/01/31/5890b107331fb.jpg)

     区别

     ?res开头的是Musixmatch提供的歌词

     timetest是YouTube（上传者）提供的歌词

     ?res 的就不上图了，查找方法与?timetext类似

     **⚠️注意**

     timetest的需要更改后面的srv1，否则无法用google2srt转换

     如这个链接

     `https://www.youtube.com/api/timedtext?hl=en_US&signature=C......rP-YP4c5I&lang=en&fmt=srv3`

     要改为srv1

     `https://www.youtube.com/api/timedtext?hl=en_US&signature=C......rP-YP4c5I&lang=en&fmt=srv1`

     最后保存为xml文件即可，若没有xml选项，保存后修改后缀为xml即可

- ## 第三步 转换歌词格式

  mv的歌词就是字幕了，一般字幕格式是srt，但我们下载的为XML，这时候就要使用一个叫做[google2srt](https://sourceforge.net/projects/google2srt/)软件转换了，google2srt这个软件也是跨平台的Mac／windows／Linux都可以使用，⚠️Mac／Linux需要安装[java](https://java.com/zh_CN/download/manual.jsp)打开jar文件，windows系统则可直接打开exe文件。

  google2srt的使用方法如图

  ![1d6e8c8773a75946.jpg](https://ooo.0o0.ooo/2017/01/31/5890b42442a14.jpg)

  可以自定义输出的srt字幕路径

  之后可以手动载入字幕或视频文件名和字幕文件名一样就可以显示字幕了

- ## *第四步 用mkvtoolnix封装字幕和视频（可选）*

  略，就是把两个文件（视频字幕）合成一个封装字幕的视频。。。

出自lioliy.ml

作者lioliy

转载请保留原文链接及作者。
