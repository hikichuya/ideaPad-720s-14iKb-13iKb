# ideaPad-720s-14iKb-13iKb
Hackintosh for ideapad 720s series （Opencore）

Opencore版本：0.7.1
已测试支持 macOS Mojave/Catalina/Big Sur/Monterey（Beta）

# 配置：
机器：Lenovo ideaPad 720s-14iKB

处理器：Intel Core-i7 8500U/UHD 620

声卡：Realtek ALC236

无线网卡：Intel AC-8265 Wireless Adapter


支持第八代酷睿的ideadPad720s，14iKb，13iKb可以使用，7代版本请手动修改声卡id和显卡id。

# 正常的工作：
引导macOS（废话）

显示卡（0x59168086，显存2048，预置EDID） 仿冒声卡（layout-id 15）

电池识别 睡眠/长睡眠及唤醒   

电源管理 处理器/GPU变频

USB定制 雷电3 储存卡 

iMessage和FaceTime

触控板和手势

（带的序列号是白果的，可以用，别改序列号否则就会用不了，但可以改机型编码）

无线网络

（带的驱动是macOS12的，其他版本系统请自行替换为其他系统版本的airportitlwm；https://github.com/OpenIntelWireless/itlwm）

蓝牙

（带的驱动是macOS12的，使用BlueToolFix.kext，测试蓝牙鼠标正常，低版本系统请替换为其他系统版本的IntelBluetoothFireware.kext，此驱动的IntelBluetoothinjector无法使用蓝牙鼠标，但其他蓝牙功能正常。https://github.com/OpenIntelWireless/IntelBluetoothFirmware）

# 不正常的功能：
HDMI接口（可以使用雷电转接）

指纹

NVIDA 独立显示卡


# 开启HIDPi

使用此处的脚本开启：https://github.com/xzhih/one-key-hidpi

开启时请勿注入EDID，除非config中预置的EDID不适合你。

建议开启以下两个分辨率：1440x810 1600x900

前者缩放150%，更加细腻；后者缩放120%，Nx900的分辨率更贴近Macbook的缩放（可以使启动台图标大小变得和白果一样）

由于显卡性能问题，开启HIDPI可能会导致卡顿！




如果由于显示问题而无法引导，建议尝试删除Config中DeviceProperties的子项中的AAPL00,override-no-connect一项，再尝试开机！
