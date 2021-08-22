# improsty-engine
 经 典 永 流 传

# 贡献规则
 本存储库接受pull请求，未防止文件混乱，要遵守如下规则

 1. 视频存放目录命名必须为原视频av号，详见目前的目录结构

 2. 视频来原必须为高质量的手机客户端缓存，请使用ffmpeg工具进行合并，并且保存文件名必须为full.mkv

 3. 对于大于100M的视频文件，请开启issue进行讨论

 4. 如果您实在不知道怎么操作，欢迎开启issue讨论，要知道规则是死的，人是活的

# 如何使用ffmpeg工具合并手机端的缓存视频

 首先安装[termux](https://f-droid.org/en/packages/com.termux/)

 *termux已经放弃对于安卓7以下版本的支持，此教程不适用于安卓7以下版本*

 *安卓10+已经不允许第三方应用读取Android目录。而且bilibili也即将不支持修改缓存目录，此教程同样不适用于安卓10+*

 使用下面的命令安装ffmpeg

    pkg in ffmpeg

 执行下面的命令，并授予termux存储权限

    termux-setup-storage

 切换工作目录为缓存视频目录

 **bilibili国内版：/sdcard/Android/data/tv.danmaku.bili/download/**

 **bilibili港澳台版:/sdcard/Android/data/com.bilibili.app.in/download/**

 *不支持bilibili国际版*

 此时该目录下所有目录的名字就为av号，此时记住av号，进入这个目录的嵌套目录的最里层，找到audio.m4s，video.m4s，用下面的命令合成视频

    ffmpeg -i audio.m4s -i video.m4s -acodec copy -vcodec copy full.mkv

 现在，你就得到了合并好的视频文件

 如果您实在不知道怎么操作，欢迎开启issue讨论，要知道规则是死的，人是活的

 ***
 
 欢迎帮助我们完善文档