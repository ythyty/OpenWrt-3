<div align="center">
<img width="768" src="https://cdn.jsdelivr.net/gh/haiibo/OpenWrt/image/openwrt.png"/>
<h1>OpenWrt — 多设备固件云编译</h1>

<img src="https://img.shields.io/github/downloads/haiibo/OpenWrt/total.svg?style=for-the-badge&color=green"/>
<img src="https://img.shields.io/github/stars/haiibo/OpenWrt.svg?style=for-the-badge&color=orange"/>
<img src="https://img.shields.io/github/forks/haiibo/OpenWrt.svg?style=for-the-badge&color=ff69b4"/>
<img src="https://img.shields.io/github/license/haiibo/OpenWrt.svg?style=for-the-badge&color=blueviolet"/>

[![](https://img.shields.io/badge/-目录:-696969.svg)](#readme) [![](https://img.shields.io/badge/-项目说明-FFFFFF.svg)](#项目说明-) [![](https://img.shields.io/badge/-固件下载-FFFFFF.svg)](#固件下载-) [![](https://img.shields.io/badge/-近期更新-FFFFFF.svg)](#近期更新-) [![](https://img.shields.io/badge/-插件预览-FFFFFF.svg)](#插件预览-) [![](https://img.shields.io/badge/-编译教程-FFFFFF.svg)](#编译教程-) [![](https://img.shields.io/badge/-文件说明-FFFFFF.svg)](#文件说明-) [![](https://img.shields.io/badge/-特别提示-FFFFFF.svg)](#特别提示-) [![](https://img.shields.io/badge/-捐助项目-FFFFFF.svg)](#捐助项目-) [![](https://img.shields.io/badge/-鸣谢-FFFFFF.svg)](#鸣谢-)
</div>


## 项目说明 [![](https://img.shields.io/badge/-项目基本介绍-FFFFFF.svg)](#项目说明-)
- 固件来源：[![Lean](https://img.shields.io/badge/Lede-Lean-red.svg?style=flat&logo=appveyor)](https://github.com/coolsnowwolf/lede) [![P3TERX](https://img.shields.io/badge/OpenWrt-P3TERX-blueviolet.svg?style=flat&logo=appveyor)](https://github.com/P3TERX/Actions-OpenWrt) [![Sirpdboy](https://img.shields.io/badge/Package-Sirpdboy-orange.svg?style=flat&logo=appveyor)](https://github.com/sirpdboy/sirpdboy-package) [![Haiibo](https://img.shields.io/badge/Build-Haiibo-success.svg?style=flat&logo=appveyor)](https://github.com/haiibo/OpenWrt)
- 项目使用 Github Actions 拉取 [Lean](https://github.com/coolsnowwolf/lede) 的 `Openwrt` 源码仓库进行云编译
- 设置定时自动编译（北京时间每天早上6点左右自动触发编译）
- 固件默认 IP 地址：`10.10.10.10` 默认密码：`password`
- 适配的软路由设备有：`X86_64`、`NanoPi_R2C`、`NanoPi_R2S`、`NanoPi_R4S`
- 适配的 ARM 盒子设备有：`微加云`、`贝壳云`、`我家云`、`斐讯N1`、`章鱼星球`、`S905x3`（包括常见的 `HK1`、`H96`、`X96` 等盒子）、`S922x`（目前支持 `GT-King`、`GT-King Pro`、`Odroid N2` 三款盒子）
- ARM 盒子固件分为 [Mini版](https://github.com/haiibo/OpenWrt/releases/tag/ARMv8_MINI) 和 [Plus版](https://github.com/haiibo/OpenWrt/releases/tag/ARMv8_PLUS)，Mini 精简版适合科学上网为主要需求的用户，Plus 多功能版插件多适合喜欢折腾的用户
- 仓库编译的固件插件均为最新版本，最新版意味着可能有 BUG，如果之前使用稳定，则无需追新
- 如固件使用有什么问题，可以直接在 [Issues](https://github.com/haiibo/OpenWrt/issues) 内留言，我会根据大家的问题进行修改
- 喜欢的可以给个 Star，感谢各位！想要自己编译固件的请看下方编译教程！


## 固件下载 [![](https://img.shields.io/badge/-编译状态及下载链接-FFFFFF.svg)](#固件下载-)
点击下表中 [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?style=flat&logo=hack-the-box)](https://github.com/haiibo/OpenWrt/releases) 即可跳转到该设备固件下载页面
| 序号 | 平台+设备名称 | 固件编译状态 | 插件配置 | 固件下载 |
| :-------------: | :-------------: | :-------------: | :-------------: | :-------------: |
| 1 | [![](https://img.shields.io/badge/OpenWrt-X86_64位-green.svg?logo=openwrt)](https://github.com/haiibo/OpenWrt/blob/main/.github/workflows/X86_64-OpenWrt.yml) | [![](https://github.com/haiibo/OpenWrt/actions/workflows/X86_64-OpenWrt.yml/badge.svg)](https://github.com/haiibo/OpenWrt/actions/workflows/X86_64-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/haiibo/OpenWrt/blob/main/x86/.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/haiibo/OpenWrt/releases/tag/X86_64) |
| 2 | [![](https://img.shields.io/badge/OpenWrt-ARMv8_Mini-green.svg?logo=openwrt)](https://github.com/haiibo/OpenWrt/blob/main/.github/workflows/ARMv8_Mini-OpenWrt.yml) | [![](https://github.com/haiibo/OpenWrt/actions/workflows/ARMv8_Mini-OpenWrt.yml/badge.svg)](https://github.com/haiibo/OpenWrt/actions/workflows/ARMv8_Mini-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/haiibo/OpenWrt/blob/main/armv8/mini/.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/haiibo/OpenWrt/releases/tag/ARMv8_MINI) |
| 3 | [![](https://img.shields.io/badge/OpenWrt-ARMv8_Plus-green.svg?logo=openwrt)](https://github.com/haiibo/OpenWrt/blob/main/.github/workflows/ARMv8_Plus-OpenWrt.yml) | [![](https://github.com/haiibo/OpenWrt/actions/workflows/ARMv8_Plus-OpenWrt.yml/badge.svg)](https://github.com/haiibo/OpenWrt/actions/workflows/ARMv8_Plus-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/haiibo/OpenWrt/blob/main/armv8/plus/.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/haiibo/OpenWrt/releases/tag/ARMv8_PLUS) |
| 4 | [![](https://img.shields.io/badge/OpenWrt-NanoPi_R2C-green.svg?logo=openwrt)](https://github.com/haiibo/OpenWrt/blob/main/.github/workflows/NanoPi_R2C-OpenWrt.yml) | [![](https://github.com/haiibo/OpenWrt/actions/workflows/NanoPi_R2C-OpenWrt.yml/badge.svg)](https://github.com/haiibo/OpenWrt/actions/workflows/NanoPi_R2C-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/haiibo/OpenWrt/blob/main/nanopi/r2c.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/haiibo/OpenWrt/releases/tag/NanoPi_R2C) |
| 5 | [![](https://img.shields.io/badge/OpenWrt-NanoPi_R2S-green.svg?logo=openwrt)](https://github.com/haiibo/OpenWrt/blob/main/.github/workflows/NanoPi_R2S-OpenWrt.yml) | [![](https://github.com/haiibo/OpenWrt/actions/workflows/NanoPi_R2S-OpenWrt.yml/badge.svg)](https://github.com/haiibo/OpenWrt/actions/workflows/NanoPi_R2S-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/haiibo/OpenWrt/blob/main/nanopi/r2s.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/haiibo/OpenWrt/releases/tag/NanoPi_R2S) |
| 6 | [![](https://img.shields.io/badge/OpenWrt-NanoPi_R4S-green.svg?logo=openwrt)](https://github.com/haiibo/OpenWrt/blob/main/.github/workflows/NanoPi_R4S-OpenWrt.yml) | [![](https://github.com/haiibo/OpenWrt/actions/workflows/NanoPi_R4S-OpenWrt.yml/badge.svg)](https://github.com/haiibo/OpenWrt/actions/workflows/NanoPi_R4S-OpenWrt.yml) | [![](https://img.shields.io/badge/编译-配置-orange.svg?logo=apache-spark)](https://github.com/haiibo/OpenWrt/blob/main/nanopi/r4s.config) | [![](https://img.shields.io/badge/下载-链接-blueviolet.svg?logo=hack-the-box)](https://github.com/haiibo/OpenWrt/releases/tag/NanoPi_R4S) |

**提示：**[![](https://img.shields.io/badge/设备-passing-32CD32.svg?logo=github)](https://github.com/haiibo/OpenWrt/actions) 标志为正常，[![](https://img.shields.io/badge/设备-failing-DC143C.svg?logo=github)](https://github.com/haiibo/OpenWrt/actions) 不代表所有编译均失败，请点击 [![](https://img.shields.io/badge/设备-状态-32CD32.svg?logo=github)](https://github.com/haiibo/OpenWrt/actions) 到 Actions 进一步查看


## 近期更新 [![](https://img.shields.io/badge/-近期固件更新-FFFFFF.svg)](#近期更新-)
🤣努力修复中……


## 插件预览 [![](https://img.shields.io/badge/-固件插件及功能预览-FFFFFF.svg)](#插件预览-)
<details>
<summary><b>&nbsp;ARM 盒子 Mini 精简版本插件预览</b></summary>
<br/>
<img src="https://cdn.jsdelivr.net/gh/haiibo/OpenWrt/image/mini.jpg"/>
</details>

<details>
<summary><b>&nbsp;ARM 盒子 Plus 多功能版插件预览</b></summary>
<br/>
<img src="https://cdn.jsdelivr.net/gh/haiibo/OpenWrt/image/plus.jpg"/>
</details>

<details>
<summary><b>&nbsp;X86、R2C、R2S、R4S 插件预览</b></summary>
<br/>
<details>
<summary><b>├── 状态</b></summary>
　├── 概况<br/>
　├── 防火墙<br/>
　├── 路由表<br/>
　├── 系统日志<br/>
　├── 内核日志<br/>
　├── 系统进程<br/>
　├── 实时信息<br/>
　├── 实时监控<br/>
　├── 负载均衡<br/>
　└── 释放内存
</details>
<details>
<summary><b>├── 系统</b></summary>
　├── 系统<br/>
　├── 管理权<br/>
　├── TTYD 终端<br/>
　├── 软件包<br/>
　├── 启动项<br/>
　├── 计划任务<br/>
　├── 挂载点<br/>
　├── 磁盘管理<br/>
　├── 高级设置<br/>
　├── LED 配置<br/>
　├── 备份/升级<br/>
　├── 文件管理<br/>
　├── 定时重启<br/>
　├── 文件传输<br/>
　├── Argon 主题设置<br/>
　└── 重启<br/>
　└── 关机
</details>
<details>
<summary><b>├── 服务</b></summary>
　├── PassWall<br/>
　├── 甜糖心愿自动采集<br/>
　├── Hello World<br/>
　├── Adblock Plus+<br/>
　├── iKoolProxy 滤广告<br/>
　├── Bypass<br/>
　├── 广告屏蔽大师 Plus+<br/>
　├── AdGuard Home<br/>
　├── 京东签到服务<br/>
　├── ShadowSocksR Plus+<br/>
　├── 易友云文件管理器<br/>
　├── DDNS.to内网穿透<br/>
　├── 微信推送<br/>
　├── 全能推送<br/>
　├── MosDNS<br/>
　├── 上网时间控制<br/>
　├── 解锁网易云灰色歌曲<br/>
　├── OpenClash<br/>
　├── 动态 DNS<br/>
　├── WiFi 计划<br/>
　├── SmartDNS<br/>
　├── 网络唤醒<br/>
　├── 迅雷快鸟<br/>
　├── UU游戏加速器<br/>
　├── Frps<br/>
　├── Frp 内网穿透<br/>
　├── AirPlay 2 音频接收<br/>
　├── Gost<br/>
　├── KMS 服务器<br/>
　├── uHTTPd<br/>
　├── udpxy<br/>
　├── UPnP<br/>
　├── Nps 内网穿透<br/>
　├── Docker CE 容器<br/>
　└── MWAN3 分流助手
</details>
<details>
<summary><b>├── Docker</b></summary>
　├── 概览<br/>
　├── 容器<br/>
　├── 镜像<br/>
　├── 网络<br/>
　├── 存储卷<br/>
　├── 事件<br/>
　└── 设置
</details>
<details>
<summary><b>├── 网络存储</b></summary>
　├── NFS 管理<br/>
　├── 阿里云盘 WebDAV<br/>
　├── 微力同步<br/>
　├── qBittorrent<br/>
　├── USB 打印服务器<br/>
　├── 硬盘休眠<br/>
　├── Transmission<br/>
　├── 挂载 SMB 网络共享<br/>
　├── 网络共享<br/>
　├── FTP 服务器<br/>
　├── Rclone<br/>
　├── Aria2 配置<br/>
　└── miniDLNA
</details>
<details>
<summary><b>├── VPN</b></summary>
　├── V2ray 服务器<br/>
　├── SoftEther VPN 服务器<br/>
　├── OpenVPN 服务器<br/>
　├── PPTP VPN 服务器<br/>
　├── IPSec VPN 服务器<br/>
　└── ZeroTier
</details>
<details>
<summary><b>├── 网络</b></summary>
　├── 接口<br/>
　├── 无线<br/>
　├── DHCP/DNS<br/>
　├── 主机名<br/>
　├── IP/MAC 绑定<br/>
　├── 静态路由<br/>
　├── 防火墙<br/>
　├── 诊断<br/>
　├── Socat<br/>
　├── 应用过滤<br/>
　├── 网速控制<br/>
　├── 多线多拨<br/>
　├── 负载均衡<br/>
　└── Turbo ACC 网络加速
</details>
<details>
<summary><b>├── 带宽监控</b></summary>
　├── 显示<br/>
　├── 配置<br/>
　├── 备份<br/>
　└── 实时流量监测
</details>
　└── <b>退出</b>
</details>


## 编译教程 [![](https://img.shields.io/badge/-项目基本编译教程-FFFFFF.svg)](#编译教程-)
1. 点击右上角 `Fork`，Fork 本项目到你自己的仓库

2. 创建个人访问令牌，如果已创建请跳过第三步（固件发布会调用，否则无法发布）

3. 点击右上角自己头像 → `Settings` → `Developer settings` → `Personal access tokens` → `Generate new token` Note 名字随便写一个，勾选 `repo` 和 `workflow` 点击最下方绿色按钮 `Generate token` 完成创建

4. 编辑对应文件夹下 `.config` 文件，`luci-app-xxx` 为插件名，结尾 `=y` 为选择，`is not set` 为不选择

5. 插件对应名称及功能请参考恩山网友帖子：[OpenWrt 编译 LuCI -> Applications 添加插件应用说明-L大](https://www.right.com.cn/forum/thread-3682029-1-1.html)

6. 如果需要修改默认 IP、添加或删除插件源以及一些其他自定义设置请在 `diy-part2.sh` 文件中进行修改

7. 点击 `Actions` → `要编译的workflow` → `Run workflow` → `Run workflow` 一次编译大概需要3~5小时

8. 编译完成后在仓库主页 `Releases` 对应 Tag 标签中查看以及下载固件

<details>
<summary><b>&nbsp;如果你觉得修改 .config 文件麻烦，那么你可以点击此处尝试本地提取</b></summary>

1. 首先安装好 Ubuntu 64bit，推荐 Ubuntu 20.04 LTS x64

2. 命令行输入 `sudo apt-get update`，然后输入
`sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch python3 python2.7 unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler g++-multilib antlr3 gperf wget curl swig rsync`

3. 使用 `git clone https://github.com/coolsnowwolf/lede` 命令下载好源代码，然后 `cd lede` 进入目录

4. 复制 diy-part2.sh 文件内所有内容到命令行，添加自定义插件和自定义设置

5. ```bash
   ./scripts/feeds update -a
   ./scripts/feeds install -a
   make menuconfig
   ```

6. 选好插件后输入以下命令导出差异部分

   ```bash
   make defconfig
   ./scripts/diffconfig.sh > seed.config
   ```

7. 这样配置的差异部分就写入 seed.config 这个文件了
   
   在命令行输入 `cat seed.config` 查看这个文件，也可以用文本编辑器打开

8. 复制 seed.config 文件内所有内容到对应 .config 文件中覆盖就可以了

   **如果不懂编译界面可以参考 YouTube 视频：[软路由固件 OpenWrt 编译界面设置](https://www.youtube.com/watch?v=jEE_J6-4E3Y&list=WL&index=7)**
</details>


## 文件说明 [![](https://img.shields.io/badge/-仓库目录文件说明-FFFFFF.svg)](#文件说明-)
```
 OpenWrt
 ├── .github/workflows
 │   ├── ARMv8-Package.yml                      # 用编译好的 ARMv8 临时固件进行打包
 │   ├── ARMv8_Mini-OpenWrt.yml                 # ARM 盒子精简版本 OpenWrt 固件编译与打包
 │   ├── ARMv8_Plus-OpenWrt.yml                 # ARM 盒子多功能版 OpenWrt 固件编译与打包
 │   ├── NanoPi_R2C-OpenWrt.yml                 # NanoPi_R2C OpenWrt 固件编译
 │   ├── NanoPi_R2S-OpenWrt.yml                 # NanoPi_R2S OpenWrt 固件编译
 │   ├── NanoPi_R4S-OpenWrt.yml                 # NanoPi_R4S OpenWrt 固件编译
 │   ├── X86_64-OpenWrt.yml                     # X86_64 OpenWrt 固件编译
 │   └── Delete-Older-Artifacts.yml             # 删除旧版本和工件
 │
 ├── armv8                                      # ARM 盒子相关代码文件
 │   ├── mini
 │   │   ├── .config                            # ARM 盒子精简版配置文件
 │   │   ├── diy-part1.sh                       # DIY 脚本第1部分
 │   │   └── diy-part2.sh                       # DIY 脚本第2部分
 │   └── plus
 │       ├── .config                            # ARM 盒子多功能版配置文件
 │       ├── diy-part1.sh                       # DIY 脚本第1部分
 │       └── diy-part2.sh                       # DIY 脚本第2部分
 │
 ├── nanopi                                     # R2C、R2S、R4S 相关代码文件
 │   ├── r2c.config                             # R2C 配置文件
 │   ├── r2s.config                             # R2S 配置文件
 │   ├── r4s.config                             # R4S 配置文件
 │   ├── diy-part1.sh                           # DIY 脚本第1部分
 │   └── diy-part2.sh                           # DIY 脚本第2部分
 │
 ├── x86                                        # X86 软路由相关代码文件
 │   ├── .config                                # X86 配置文件
 │   ├── diy-part1.sh                           # DIY 脚本第1部分
 │   └── diy-part2.sh                           # DIY 脚本第2部分
 │
 ├── LICENSE                                    # 许可文件
 └── README.md                                  # 自述文件
```


## 特别提示 [![](https://img.shields.io/badge/-个人免责声明-FFFFFF.svg)](#特别提示-)

- **因精力有限不提供任何技术支持和教程等相关问题解答，不保证完全无 BUG！**

- **本人不对任何人因使用本固件所遭受的任何理论或实际的损失承担责任！**

- **本人保证固件没加入任何后门，保护干净安全的网络环境从我做起！**


## 捐助项目 [![](https://img.shields.io/badge/-请我喝咖啡啦-FFFFFF.svg)](#捐助项目-)

**如果你觉得此项目对你有帮助，可以捐助我们，以鼓励项目能持续发展，更加完善！**

**你们的支持就是作者前进的动力！**

### 捐助方式
| <img src="https://img.shields.io/badge/-支付宝-1678FF.svg" height="25" href="#赞助支持本项目-"/> | <img src="https://img.shields.io/badge/-微信-22AB39.svg" height="25" href="#赞助支持本项目-"/> |
| :-------------: | :-------------: |
| <img src="https://user-images.githubusercontent.com/85640068/149810593-b27af61f-71c7-4a13-9f33-4e04ff2978c1.jpg" width="150" height="150" href="#赞助支持本项目-"/> | <img src="https://user-images.githubusercontent.com/85640068/149810694-a181e062-0d71-4fd9-9279-3f9ab0128b7f.jpg" width="150" height="150" href="#赞助支持本项目-"/> |


## 鸣谢 [![](https://img.shields.io/badge/-跪谢各大佬-FFFFFF.svg)](#鸣谢-)
| [ImmortalWrt](https://github.com/immortalwrt) | [coolsnowwolf](https://github.com/coolsnowwolf) | [P3TERX](https://github.com/P3TERX) | [Flippy](https://github.com/unifreq) |
| :-------------: | :-------------: | :-------------: | :-------------: |
| <img width="100" src="https://avatars.githubusercontent.com/u/53193414"/> | <img width="100" src="https://avatars.githubusercontent.com/u/31687149"/> | <img width="100" src="https://avatars.githubusercontent.com/u/25927179"/> | <img width="100" src="https://avatars.githubusercontent.com/u/39355261"/> |
| [Ophub](https://github.com/ophub) | [Jerrykuku](https://github.com/jerrykuku) | [QiuSimons](https://github.com/QiuSimons) | [IvanSolis1989](https://github.com/IvanSolis1989) |
| <img width="100" src="https://avatars.githubusercontent.com/u/68696949"/> | <img width="100" src="https://avatars.githubusercontent.com/u/9485680"/> | <img width="100" src="https://avatars.githubusercontent.com/u/45143996"/> | <img width="100" src="https://avatars.githubusercontent.com/u/44228691"/> |


<a href="#readme">
<img src="https://img.shields.io/badge/-返回顶部-FFFFFF.svg" title="返回顶部" align="right"/>
</a>
