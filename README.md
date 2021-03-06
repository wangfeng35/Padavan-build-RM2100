# Padavan-build说明
现在不需要新建Release了，已经更改了脚本，直接fork，修改好之后，点击右上角的 Star 星星按钮即可开始自动编译（自己点击才会编译）。


# 参数说明(自理解仅供参考)
- 默认登陆IP:192.168.2.1
- 默认用户名/密码:admin/admin
- 默认wifi密码:1234567890

- [C 大支持设备](#Device)
- [C 大插件分类和说明](#Plugins)

## Device

- MI-R3P(感谢群里emmmm适配,可能led控制有点问题,其它功能正常)
- 京东云路由(文件来自Lintel) 编译代码: JDC-1
- 歌华链(感谢群里Heaven适配与测试）编译代码: GHL
- NEWIFI-D1
- B70(感谢Untitled提供荒野无灯的适配文件)
- JCG-AC856M(感谢群里的旅途中的我适配和测试,gpio值还未完全适配，但不影响使用)
- JCG-AC836M(感谢群里的碧霄客修改和测试)
- YK-L1(L1、L1C、L1W通刷)
- PSG712
- PSG1208
- PSG1218
- 5K-W20 (USB)
- OYE-001 (USB)
- NEWIFI-MINI (USB)
- MI-MINI (USB)
- MI-3 (USB)
- MI-R3G (USB)
- HC5661A
- HC5761A (USB)
- HC5861B
- 360P2 (USB)
- MI-NANO
- MZ-R13
- MZ-R13P
- RT-AC1200GU (USB)
- XY-C1 (USB)
- WR1200JS (USB)
- NEWIFI3 (USB)
- B70 (USB)
- A3004NS (USB)
- K2P
- K2P-USB (USB)
- JCG-836PRO (USB)
- JCG-AC860M (USB)
- DIR-882 (USB)
- DIR-878
- MR2600 (USB)
- WDR7300
- RM2100
- R2100

## Plugins

### 游戏加速

| 名字              | 变量                                |
| ---------------- | ----------------------------------- |
| [SS plus+][ss+]  | CONFIG_FIRMWARE_INCLUDE_SHADOWSOCKS |
| [SS server][sss] | CONFIG_FIRMWARE_INCLUDE_SSSERVER    |
| v2ray 执行文件    | CONFIG_FIRMWARE_INCLUDE_V2RAY       |
| trojan 执行文件   | CONFIG_FIRMWARE_INCLUDE_TROJAN      |

[ss+]: https://github.com/coolsnowwolf/lede
[sss]: https://github.com/shadowsocks/shadowsocks-libev

> 备注
>
> - 集成 v2ray 执行文件（3.8M 左右)，如果不集成，会从网上下载下来执行，不影响正常使用
> - 集成 trojan 执行文件(1.1M 左右)，如果不集成，会从网上下载下来执行，不影响正常使用

### 广告

| 名字                 | 变量                                |
| ------------------- | ----------------------------------- |
| [adbyby plus+][adb] | CONFIG_FIRMWARE_INCLUDE_ADBYBY      |
| [Kool][kp]          | CONFIG_FIRMWARE_INCLUDE_KOOLPROXY   |
| [ADGUARD][adg]      | CONFIG_FIRMWARE_INCLUDE_ADGUARDHOME |

[adb]: https://github.com/coolsnowwolf/lede
[kp]: http://koolshare.cn/thread-64086-1-1.html
[adg]: https://github.com/coolsnowwolf/lede

> 备注

### DNS 有关

| 名字                        | 变量                                 |
| -------------------------- | ------------------------------------ |
| DNSFORWARD        | CONFIG_FIRMWARE_INCLUDE_DNSFORWARDER |
| [smartdns][kp]             | CONFIG_FIRMWARE_INCLUDE_SMARTDNS     |
| [smartdns-二进制文件][adg]   | CONFIG_FIRMWARE_INCLUDE_SMARTDNSBIN  |

> 备注

### 文件

| 名字                            | 变量                          |
| -------------------------------| ----------------------------- |
| [CADDY 在线文件管理服务][caddy]   | CONFIG_FIRMWARE_INCLUDE_CADDY |
| caddy 执行文件                   | CONFIG_FIRMWARE_INCLUDE_CADDYBIN |

[caddy]: https://github.com/hacdias/filebrowser

> 备注
>
> - caddy 执行文件，此文件有 13M,请注意固件大小。如果不集成，会从网上下载下来执行，不影响正常使用

### 穿透

| 名字                  | 变量                             |
| --------------------- | ------------------------------- |
| 阿里 DDNS             | CONFIG_FIRMWARE_INCLUDE_ALIDDNS |
| [穿透客户端 FRPC][fr]  | CONFIG_FIRMWARE_INCLUDE_FRPC    |
| [穿透服务端 FRPS][fr]  | CONFIG_FIRMWARE_INCLUDE_FRPS    |

[fr]: https://github.com/fatedier/frp

> 备注

### 代理

| 名字                        | 变量                                        |
| -------------------------- | ------------------------------------------- |
| [TUNSAFE][tunsafe]         | CONFIG_FIRMWARE_INCLUDE_TUNSAFE             |
| KUMA                       | CONFIG_FIRMWARE_INCLUDE_KUMASOCKS           |
| [srelay][srelay]           | CONFIG_FIRMWARE_INCLUDE_SRELAY              |
| IPT2                       | CONFIG_FIRMWARE_INCLUDE_IPT2SOCKS           |
| MICRO                      | CONFIG_FIRMWARE_INCLUDE_MICROSOCKS          |
| [softether-vpnserver][sevpn] | CONFIG_FIRMWARE_INCLUDE_SOFTETHERVPN_SERVER |
| [softether-vpnclient][sevpn] | CONFIG_FIRMWARE_INCLUDE_SOFTETHERVPN_CLIENT |
| [softether-vpncmd][sevpn]    | CONFIG_FIRMWARE_INCLUDE_SOFTETHERVPN_CMD    |

[tunsafe]: https://github.com/TunSafe/TunSafe
[srelay]: https://socks-relay.sourceforge.io/
[sevpn]: https://github.com/SoftEtherVPN/SoftEtherVPN_Stable

> 备注

### 校园网

| 名字                                  | 变量                                 |
| ------------------------------------- | ----------------------------------- |
| [dogcom 校园网][dogcom]                | CONFIG_FIRMWARE_INCLUDE_DOGCOM      |
| [minieap][minieap]                    | CONFIG_FIRMWARE_INCLUDE_MINIEAP     |
| [SCUT][scutclient]                    | CONFIG_FIRMWARE_INCLUDE_SCUTCLIENT  |
| [drcom][drcom]                        | CONFIG_FIRMWARE_INCLUDE_GDUT_DRCOM  |
| [njit-client][njit-client]            | CONFIG_FIRMWARE_INCLUDE_NJIT_CLIENT |
| [NAPT66 教育网 ipv6][napt66]           | CONFIG_FIRMWARE_INCLUDE_NAPT66      |
| [mentohust-锐捷、赛尔认证][mentohust]   | CONFIG_FIRMWARE_INCLUDE_MENTOHUST   |

[minieap]: https://github.com/hanwckf/minieap
[dogcom]: https://github.com/hanwckf/dogcom
[drcom]: https://github.com/chenhaowen01/gdut-drcom
[scutclient]: https://github.com/hanwckf/scutclient
[njit-client]: https://github.com/hanwckf/njit8021xclient
[napt66]: https://github.com/mzweilin/napt66
[mentohust]: https://github.com/hanwckf/mentohust-1

> 备注
>
> - minieap 扩展的 802.1x 客户端，带有锐捷 v3 (v4) 算法插件支持
> - scutclient 华南理工大学
> - njit-client 南京工程学院 802.1X 客户端

### 网易云解锁
| 名字                                           | 变量                             |
| --------------------------------------------- | -------------------------------- |
| 网易云解锁  | CONFIG_FIRMWARE_INCLUDE_WYY   |
| 网易云解锁GO版本执行文件  | CONFIG_FIRMWARE_INCLUDE_WYYBIN     |

> 备注
>
> - 网易云解锁GO版本执行文件（4M多）注意固件超大小


### 其他

| 名字                                           | 变量                             |
| --------------------------------------------- | -------------------------------- |
| [vlmcsd-KMS 服务器][vlmc]                            | CONFIG_FIRMWARE_INCLUDE_VLMCSD   |
| [ttyd-网页终端][ttyd]                          | CONFIG_FIRMWARE_INCLUDE_TTYD     |
| [lrzsz-文件互传][lrzse]                        | CONFIG_FIRMWARE_INCLUDE_LRZSZ    |
| [curl][curl]                                  | CONFIG_FIRMWARE_INCLUDE_CURL     |
| [htop-进程浏览][htop]                          | CONFIG_FIRMWARE_INCLUDE_HTOP     |
| [nano-文本编辑器][nano]                        | CONFIG_FIRMWARE_INCLUDE_NANO     |
| [iperf3-网络测试][ipres3]                      | CONFIG_FIRMWARE_INCLUDE_IPERF3   |
| [dump1090-RTLSDR 设备模式 S 解码器][dump1090]   | CONFIG_FIRMWARE_INCLUDE_DUMP1090 |
| [rtl-sdr][rtl-sdr]                            | CONFIG_FIRMWARE_INCLUDE_RTL_SDR  |
| [samba3.6][samba3.6]                          | CONFIG_FIRMWARE_INCLUDE_SMBD36   |
| [mtr-网络诊断工具][mtr]                         | CONFIG_FIRMWARE_INCLUDE_MTR      |
| [socat][socat]                                | CONFIG_FIRMWARE_INCLUDE_SOCAT    |

[curl]: https://github.com/curl/curl
[vlmc]: https://github.com/hanwckf/vlmcsd
[ttyd]: https://github.com/tsl0922/ttyd
[lrzse]: https://ohse.de/uwe/software/lrzsz.html
[htop]: https://hisham.hm/htop/releases/
[nano]: https://www.nano-editor.org/dist/
[ipres3]: https://github.com/esnet/iperf
[dump1090]: https://github.com/hanwckf/dump1090
[rtl-sdr]: https://github.com/osmocom/rtl-sdr
[samba3.6]: https://gitlab.com/padavan-ng/padavan-ng/tree/master/trunk/user/samba36
[rtl-sdr]: https://github.com/osmocom/rtl-sdr
[mtr]: https://github.com/traviscross/mtr
[socat]: http://www.dest-unreach.org/socat

> 备注
>
> - rtl-sdr 实现 USB 接口的接收机
> - samba3.6 实现 SMB 协议
> - socat 个多功能的网络工具

# 鸣谢
- upbit自动编译脚本：https://github.com/upbit/Padavan-build-RM2100
- chongshengB源码：https://github.com/chongshengB/rt-n56u
- hanwckf源码：https://github.com/hanwckf/rt-n56u
- lean源码: https://github.com/coolsnowwolf/lede
- 汉化字典来自：https://github.com/gorden5566/padavan
- hanwckf更新日志：https://www.jianshu.com/p/d76a63a12eae
- 固件使用说明：https://www.jianshu.com/p/cb51fb0fb2ac
- 固件编译办法：https://www.jianshu.com/p/6b8403cdea46
