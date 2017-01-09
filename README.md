# BeagleBoneBlack
黑骨犬单板微型嵌入式计算机

## 启动

参考链接:

* http://processors.wiki.ti.com/index.php/Processor_SDK_Linux_Software_Developer%E2%80%99s_Guide
* http://processors.wiki.ti.com/index.php/Processor_SDK_RTOS_Software_Developer_Guide
* http://www.ti.com/lsds/ti/tools-software/processor_sw.page
* http://ellcc.org/
* http://ronubo.blogspot.com/2016/02/u-boot-over-qemu-arm.html
* https://wiki.ubuntu.com/Kernel/Dev/QemuARMVexpress

### U-Boot
* http://processors.wiki.ti.com/index.php/Linux_Core_U-Boot_User%27s_Guide#Working_with_USB_Device_Firmware_Upgrade
* http://processors.wiki.ti.com/index.php/AM335x_U-Boot_User's_Guide
* https://training.ti.com/linux-board-porting-training-series
* https://eewiki.net/display/linuxonarm/BeagleBone+Black
* http://elinux.org/Beagleboard:U-boot_partitioning_layout_2.0

### 玩转BeagleBoneBlack

1. http://processors.wiki.ti.com/index.php/Processor_SDK_Linux_Setup_Script
2. http://elinux.org/Beagleboard:Updating_The_Software
3. http://elinux.org/Mount_BeagleBoard_Root_Filesystem_over_NFS_via_USB
4. http://derekmolloy.ie/

### 运行ubuntu

* http://elinux.org/BeagleBoardUbuntu#BeagleBone_White.2FBlack.2FGreen

### USB走串口

黑犬板上自带串口，但还需要额外购买一根串口线才能跟电脑相连．这个实验重新配置uboot和内核
以便把板上USB转成串口来使用. 为此, 板载eMMC和TF卡各自带有一个可以运行的系统, 拿eMMC上
的系统来做实验, TF卡当作拯救盘. 当前两个系统都配置成USB走网络.

##### 黑犬板启动顺序

1. 默认启动顺序: eMMC(MMC1)-> MicroSD(MMC0)->UART0->USB0
2. 加电时按住S2按钮: SPI0->MicroSD(MMC0)->USB0->UART0


参考链接群:

* http://elinux.org/Beagleboard:BeagleBoneBlack#Revision_C_.28Production_Version.29
* http://processors.wiki.ti.com/index.php/The_Boot_Process

