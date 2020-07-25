### 华硕FX53VD OPENCORE 0.5.6引导文件

#### 笔记本配置
|规格 | 详细信息|
|:-: | :-:|
|电脑型号|华硕FX53VD|
|操作系统|macOS Catalina 10.15.4 |
|处理器|英特尔 酷睿 i5-7300HQ|
|内存|16GB DDR4|
|显卡|Intel HD Graphics 630|
|显示器|15.6 英寸 IPS 1920x1080|
|声卡| Realtek ALC235|

#### 配置修改备忘:
1. Booter-Quirks-DisableVariableWrite: False NVRAM可以写入数据，重启不丢失
2. Misc-Boot-HideAuxiliary: True 隐藏一些不需要的启动项
3. Misc-Boot-PickerMode: Builtin 使用oc的启动选择器不要图形界面
4. Misc-Boot-ShowPicker: False 不显示启动选择界面 (第一次启动时用True，不然选不了启动项)
5. Misc-Boot-Timeout: 0 直接进入系统 (第一次启动时设为5，不然选不了启动项)
6. Misc-Boot-Tools: 全部禁用
7. NVRAM-Add-7C436110-AB2A-4BBB-A880-FE41995C9F82-`csr-active-config`: `<E7030000>` 关闭SIP
8. NVRAM-LegacyEnable: False 禁用模拟nvram
9. NVRAM-WriteFlash: True 系统偏好设置-启动磁盘-可以设置默认启动项
10. PlatformInfo-Generic-ROM: 数据类型改为Data，启动屏幕不报错

#### OC文件来源
[QiuChenly/ASUS_FX53VD_ZX53VD_FX86FE_EFI](https://github.com/QiuChenly/ASUS_FX53VD_ZX53VD_FX86FE_EFI "原始来源")
