# 【分享】菜鸟都知道Sigpatch签名补丁和SW系统、大气层的关系

当前SW17.0.0系统还缺少FS补丁，很多菜鸟连sigpatch也不懂，莱莱不是大佬，但是这点基本的常识还是想和各位小伙伴们普及，免得大家以后闹笑话。

当前是17.0.0最新系统，但是Sigpatch还缺17.0.0的FS补丁，最高只有16.1.0，更新大气层1.6.1的破解包以后完全可以：

正版系统升级到17.0.0，能正常玩正版游戏。

虚拟系统升级到16.1.0，能正常玩破解游戏。

1、大气层sigpatch签名补丁=允许大气层破解SW系统以后能玩安装和玩NSP，XCI等破解游戏或者NSP自制软件。

大气层作者支持破解，但不支持玩破解游戏。当前的大气层sigpatch签名补丁就是包括ES、FS、NIFM补丁和Loader补丁，只有正确的签名补丁对应SW系统和大气层才能正常玩破解游戏。

2、ES补丁在TF卡atmosphere/exefs_patches/es_patches，对应SW系统，每次SW系统大版本升级会需要新增1个IPS。

当前17.0.0最新系统，新增17.0.0的ES补丁以后，一共是25个IPS文件。

ES补丁允许你从Eshop商店dump出来的原版NSP（含压缩格式NSZ）游戏文件安装和正常运行。

3、FS补丁在TF卡的atmosphere/kip_patches/fs_patches，对应SW系统，每次SW系统大版本升级会需要新增2个IPS（exfat和fat32）。

当前17.0.0最新系统，但只有最高16.1.0的FS补丁，一共是51个IPS文件，因为SW1.0系统无exfat驱动。

FS补丁允许你使用非原版NSP文件（NSP，NSZ，XCI，XCZ）的安装和正常运行，包括NRO转NSP的自制软件，整合版XCI，NSP等格式的游戏安装包。

4、NIFM补丁在TF卡的atmosphere/exefs_patches/nfim_ctest，和SW系统有关，每次SW系统大版本升级会需要新增1个IPS。

当前17.0.0最新系统，新增17.0.0的NIFM补丁以后，一共是24个IPS文件。

NIFM补丁是忽略主机联网后强制连任天堂服务器认证的补丁。

5、ES、FS、NIFM这三个补丁是和SW系统有关，虽然理论上最好齐全，这样SW系统降级以后也能正常玩破解游戏，但是又有哪个NTR会降级系统到很低的版本呢？Switch现在的破解，降级到很低的系统有什么意思，是闲的慌还是脑子不好使了？

所以ES、FS、NIFM这三个补丁，实际上保留2-3个新版本就够了，比如当前17.0.0最新，保留对应SW16.0和SW16.1的几个补丁也完全够了，其它的IPS文件想删就删，不影响玩破解游戏。

6、Loader补丁在TF卡的atmosphere/kip_patches/loader_patches，对应大气层package3，每次大气层版本升级需要新增1个IPS，但是可以删除旧的大气层Loader补丁，大气层向下兼容，降级SW系统也不需要更换大气层整合包。

当前大气层1.6.1最新版本，新增大气层1.6.1的Loader补丁，只需要1个IPS文件。

7、大气层系统分fss0引导（真实系统、虚拟系统、机身正版系统）和fusee引导（自动选择）。

fss0引导的ES补丁和nfim补丁与fusee引导一样，没有区别。

fss0引导的FS补丁和Loader补丁在TF卡的bootloader/patches.ini，不同于fusee引导。

fss0引导，还要在Bootloader/Hekate_ipl.ini中添加“kip1patch=nosigchk”。
