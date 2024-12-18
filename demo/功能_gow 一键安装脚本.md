

# 功能_gow 一键安装脚本

## 功能说明
- 科学上网，走向世界
- 脚本一键安装：
    - 1. PASSWALL
    - 2. PASSWALL2
    - 3. SSR+
    - 4. OpenVPN

## 安装步骤

1. **登录后台管理界面**

   - 输入产品背标上的后台 IP 地址，进入后台管理界面：
    ![IP](/docs/img/fcc867427d022ca11bfdcbc8cd42f16.png)

2. **进入 TTYD 终端**

   - 在后台管理界面左侧菜单中，选择 **应用程序** -> **TTYD 终端**。
    ![TTyd](/docs/img/ttyd.png)

3. **登录终端**

   - 打开 TTYD 终端后，系统会提示你输入登录用户名。
   - 输入 `root` 然后按回车。
   - 接着系统会提示输入密码。默认密码是 `admin`，输入密码后按回车（注意：密码输入时不会显示，输入完成后直接按回车即可）。如果你已经修改了密码，请输入你自己的密码：
     ![登录界面](/docs/img/luci_ttyd.png)

   - 登录成功后，终端会显示如下内容：
     ```
     root@openwrt :~#
     ```

4. **执行安装脚本**

   - 在终端中粘贴以下命令，并按回车执行：
     ```sh
     wget -O /tmp/gow.sh "http://dl.nextfi.link/mt7621/gow.sh" && chmod +x /tmp/gow.sh && sh /tmp/gow.sh
     ```

5. **等待脚本执行完成**

   - 根据提示，按步骤操作并等待脚本执行完成。整个过程需要一定的时间，请耐心等待：
    ```sh
    BusyBox v1.36.0 (2024-08-17 05:42:22 UTC) built-in shell (ash)

     _________
    /        /\      _    ___ ___  ___
   /  LE    /  \    | |  | __|   \| __|
  /    DE  /    \   | |__| _|| |) | _|
 /________/  LE  \  |____|___|___/|___|
 \        \   DE /
  \    LE  \    /  -------------------------------------------
   \  DE    \  /    OpenWrt SNAPSHOT, r6854-2ffed5362
    \________\/    -------------------------------------------

root@OpenFi:~# wget -O /tmp/gow.sh "http://dl.nextfi.link/mt7621/gow.sh" && chmod +x /tmp/gow.sh && sh /tmp/gow.sh
--2024-12-18 19:49:03--  http://dl.nextfi.link/mt7621/gow.sh
Resolving dl.nextfi.link... 198.18.3.23
Connecting to dl.nextfi.link|198.18.3.23|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2329 (2.3K) [text/plain]
Saving to: '/tmp/gow.sh'

/tmp/gow.sh                                         100%[================================================================================================================>]   2.27K  --.-KB/s    in 0s      

2024-12-18 19:49:04 (17.0 MB/s) - '/tmp/gow.sh' saved [2329/2329]

 
请选择要安装的插件：
  1. PASSWALL
  2. PASSWALL2
  3. SSR+
  4. OpenVPN
 
请输入数字:3
 
正在安装SSR+>>>...
>>>> 正在下载，请不要关闭窗口，等待下载完成后自动执行安装。
--2024-12-18 19:49:11--  http://dl.nextfi.link/mt7621/202410_ssr+.tar.gz
Resolving dl.nextfi.link... 198.18.3.23
Connecting to dl.nextfi.link|198.18.3.23|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 11016135 (11M) [text/plain]
Saving to: '/tmp/202410_ssr+.tar.gz'

/tmp/202410_ssr+.tar.gz                             100%[================================================================================================================>]  10.50M  9.14MB/s    in 1.1s    

2024-12-18 19:49:12 (9.14 MB/s) - '/tmp/202410_ssr+.tar.gz' saved [11016135/11016135]

ssr+/
ssr+/luci-i18n-ssr-plus-zh-cn_188-6_all.ipk
ssr+/0.install_guide.txt
ssr+/v2ray-core_5.16.1-1_mipsel_24kc.ipk
ssr+/shadowsocksr-libev-ssr-redir_2.5.6-11_mipsel_24kc.ipk
ssr+/shadowsocksr-libev-ssr-check_2.5.6-11_mipsel_24kc.ipk
ssr+/trojan_1.16.0-2_mipsel_24kc.ipk
ssr+/shadowsocksr-libev-ssr-local_2.5.6-11_mipsel_24kc.ipk
ssr+/luci-app-ssr-plus_188-6_all.ipk
 
>>>> 正在安装 ssr+  安装过程需要等待几分钟，请不要关闭窗口，耐心等待执行完成。
Unknown package 'luci-app-ssr-plus'.
Installing luci-i18n-ssr-plus-zh-cn (188-6) to root...
Installing shadowsocksr-libev-ssr-check (2.5.6-11) to root...
Installing v2ray-core (5.16.1-1) to root...
Installing shadowsocksr-libev-ssr-local (2.5.6-11) to root...
Installing shadowsocksr-libev-ssr-redir (2.5.6-11) to root...
Installing trojan (1.16.0-2) to root...
Installing luci-app-ssr-plus (188-6) to root...
Package shadowsocksr-libev-ssr-check (2.5.6-11) installed in root is up to date.
Package shadowsocksr-libev-ssr-local (2.5.6-11) installed in root is up to date.
Package shadowsocksr-libev-ssr-redir (2.5.6-11) installed in root is up to date.
Package trojan (1.16.0-2) installed in root is up to date.
Package v2ray-core (5.16.1-1) installed in root is up to date.
Configuring shadowsocksr-libev-ssr-check.
Configuring trojan.
Configuring v2ray-core.
Configuring shadowsocksr-libev-ssr-local.
Configuring shadowsocksr-libev-ssr-redir.
Configuring luci-app-ssr-plus.
uci: Entry not found
Configuring luci-i18n-ssr-plus-zh-cn.
uci: Entry not found
Collected errors:
 * pkg_hash_check_unresolved: cannot find dependency v2ray-plugin for luci-app-ssr-plus
 * pkg_hash_fetch_best_installation_candidate: Packages for luci-app-ssr-plus found, but incompatible with the architectures configured
 * opkg_install_cmd: Cannot install package luci-app-ssr-plus.
 * satisfy_dependencies_for: Cannot satisfy the following dependencies for luci-i18n-ssr-plus-zh-cn:
 *      v2ray-plugin
 
>>>> 已安装完成 ssr+  请进入管理界面，在服务菜单中查看。
 
>>>> 删除临时文件： /tmp/202410_ssr+.tar.gz    /tmp/mt7621_ipks/ssr+

```

6. **刷新后台管理界面**

   - 脚本执行完成后，刷新后台管理界面就可以在 **OpenWrt 原生功能菜单** 中查看到对应功能的菜单啦。
   - 如果没找到，可以尝试重启路由器。

---

### 小贴士

- **耐心等待**：执行脚本需要路由器连接到网络，并且脚本执行可能需要一些时间，要确保在整个过程中不要中断操作。
- **密码注意**：输入密码时不会显示字符，输入完成后按回车即可哦！
- **遇到问题**：如果遇到任何问题，可以尝试重新登录 TTY 终端或者检查网络连接是否正常。
