# packetCapture

安卓 7.0 及以上系统抓 app https 包方法

## 准备软件

- windows 电脑：[雷电 9 模拟器](https://www.ldmnq.com/)

- windows 电脑：[Charles](http://www.manongjc.com/detail/60-qhpkjidfnchvlto.html)

- 雷电 9 模拟器：需要抓包的 app

## 抓包步骤

1. 雷电 9 模拟器，开启 root 和 System.vmdk 可写入

2. 配置 Charles 和 雷电 9 模拟器（网上查的到）

3. 手机安装 Charles 证书，电脑 Charles 点击 Help -> SSLProxying -> Install CHarles Root Certificate on a Mobile Device or Remote Browser，然后手机打开 chls.pro/ssl 下载证书，并安装

4. 第 1 步安装的证书在用户信任的凭据下，需要复制到系统信任的凭据下，将 /data/misc/user/0/cacerts-added/ 文件夹下的 xxx.0 文件复制到 /system/etc/security/cacerts/ 文件夹下

5. 打开需要抓包的 app，就能在 Charles 看到请求了
