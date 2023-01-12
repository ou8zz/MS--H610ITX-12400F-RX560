# MS挑战者-H610ITX-12400F-560

### 平台配置 Big Sur 11.5 (OC 0.8.5)
##### 替换老的10700主力机，之前用12代es不能用PCIE浪费了一个插槽，没法发挥ITX最大性能，13代出来了，12代正式版价格现在也下来了些，考虑到Windows11的拉胯体验，还是纯大核心ITX合适。EFI仅供参考。PS：EFI中三码需要重新生成。
##### 当前EFI配置主要参考官方Cometlake的配置 https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#deviceproperties
##### 整机待机在30W左右，日常使用在30W～80W之间
```
CPU i5-12400F
主板 MS挑战者-H610ITX
内存 Kingston 8G（2400-CL16） * 2 / Tigo 8G（2400-CL16） * 2
显卡 RX560 2G
网卡 BCM94352z
SSD SanDisk Extreme Pro 500GB
散热器 is50x
机箱电源 K39套300w电源
```


### 黑苹果遇到的问题
新主板默认刷的新的支持13代CPU的bios，这个bios是锁CFGLock，并且无法通过OC设置appleCpuPmCfgLock和AppleXcpmCfgLock参数解锁，同时ControlMsrE2.efi设置解锁也不行。版本号为E1.4G，后刷回上一个版本E1.3G或者E1.2G即可。很关键。 

### 关于黑苹果的网卡问题
淘宝90入的BCM94352z这个网卡驱动后网络只有最大400m且不稳定，接力延迟很大，我在手机打开一个网页，需要等2-5秒才能在电脑上弹出浏览器的小图标，而另一台机器早就显示了，这个问题我没细纠结了。我以为是驱动问题，转到在windows环境下测试网卡及蓝牙，同样测得最大400M的网络最大速度以及蓝牙延迟，当即淘宝退款这个网卡。 

### 相关测试图片详见 https://www.bilibili.com/read/cv21154609?spm_id_from=444.41.list.card_article.click
