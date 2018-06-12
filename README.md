## 提升 mac 工作及开发效率的方法汇总

### [Karabiner Elements](https://github.com/tekezo/Karabiner-Elements)
> 键位映射神器

用 Caps Lock（也就是大小写切换键）来切换大小写是非常低效的。以输入文字 aBc 为例，我们需要按下 Caps Lock 键进入大写模式，输入 B，再按一次键回到小写模式，输入 c。正确的做法是使用 shift 键，我们按住 shift 键输入 b 就会得到大写的字母，再松开就回到了小写模式。和 Caps Lock 键相比，少了一次按键。

键盘上的 Ctrl 键位置很差，如果你是用标准的打字手势，你会发现这个键刚好在左手的手心，无论哪个手指都不方便去按它。而 Caps Lock 键则占据了左手小拇指左侧的黄金位置。更重要的是，Ctrl 键的用途非常广，无论是作为 Vim 或者 Emacs 的功能键，还是各种快捷键的修饰键，都是一个非常常用的按键。

### [Shadowsocks](https://github.com/shadowsocks)
> 不用多介绍，翻墙必备工具

[iOS 客户端](https://itunes.apple.com/us/app/shadowrocket/id932747118?mt=8)
[Android 客户端](https://github.com/shadowsocks/shadowsocks-android/releases)
[Windows 客户端](https://github.com/shadowsocks/shadowsocks-windows/releases)
[Mac 客户端](https://github.com/shadowsocks/ShadowsocksX-NG/releases)

### Homebrew 开启代理
> 由于国内网络进一步恶劣，使用 brew 也要更换国内大学的镜像源，但是这样的方法治标不治本，更新是快了，可是下载还是一样

上面使用了 Shadowsocks 之后，系统就会存在一个 socks5 的代理，基于这个代理就可以为 Homebrew 设置全局代理进行修改

```bash
$ echo export ALL_PROXY=socks5://127.0.0.1:1080 >> ~/.bash_profile

// 如果是 zsh 就下边这个
$ echo export ALL_PROXY=socks5://127.0.0.1:1080 >> ~/.zsh_profile
```
