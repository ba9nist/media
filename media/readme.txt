


此补丁包：
1.合代码。
2.libstagefright下面mm -B 进行编译
3.CedarX-Projects下面mm -B进行编译


\device\softwinner\nuclear-common\ProductCommon.mk
需修改ProductCommon.mk加入libaw_h264enc.so和libcedarxsftstream.so两个库，否者mediaserver启动失败，导致进入不了luancher。



如果启动没到luancher界面，请把so手动推到盒子。
adb push libaw_h264enc.so /system/lib/
adb push libcedarxsftstream.so /system/lib/

注意：
libmediaplayerservice 和 libstagefright  一定要重新编译，否则会出现头文件不一致导致任何视频都不能播放。。。

