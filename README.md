# BTinstall_6.0
宝塔面板7.7原版安装脚本

宝塔面板7.8版本使用各种方法均无法绕过绑定账号，并且不绑定账号无法下载安装插件。

因此这里分享一下7.7版本的安装脚本，是官方免费版的。
```
wget -O install.sh https://raw.githubusercontent.com/php-garlic/BTinstall_6.0/main/install_6.0.sh && bash install.sh
```


建议配合下面文章中的优化脚本使用：
这个是根据个人使用习惯做的宝塔面板一键优化补丁，主要有以下优化项目：
1.去除宝塔面板强制绑定账号
2.去除各种删除操作时的计算题与延时等待
3.去除创建网站自动创建的垃圾文件（index.html、404.html、.htaccess）
4.关闭未绑定域名提示页面，防止有人访问未绑定域名直接看出来是用的宝塔面板
5.关闭活动推荐与在线客服
```
wget -O optimize.sh https://raw.githubusercontent.com/insoxin/BTinstall_6.0/main/optimize.sh && bash optimize.sh

```



## 手动升级
1、选择版本
http://download.bt.cn/install/update/LinuxPanel-5.9.1.zip（目前仍然很多人在用的版本）
http://download.bt.cn/install/update/LinuxPanel-7.0.1.zip
http://download.bt.cn/install/update/LinuxPanel-7.0.2.zip
http://download.bt.cn/install/update/LinuxPanel-7.0.3.zip
http://download.bt.cn/install/update/LinuxPanel-7.1.0.zip
http://download.bt.cn/install/update/LinuxPanel-7.1.1.zip
http://download.bt.cn/install/update/LinuxPanel-7.2.0.zip
http://download.bt.cn/install/update/LinuxPanel-7.3.0.zip
http://download.bt.cn/install/update/LinuxPanel-7.4.0.zip
http://download.bt.cn/install/update/LinuxPanel-7.4.2.zip （有pma漏洞）
http://download.bt.cn/install/update/LinuxPanel-7.4.3.zip
http://download.bt.cn/install/update/LinuxPanel-7.4.5.zip（会有绑定提醒）
http://download.bt.cn/install/update/LinuxPanel-7.7.0.zip

2、官方给出的手动升级方法
离线升级步骤：
1、下载离线升级包
2、将升级包上传到服务器中的/root目录
3、解压文件：unzip LinuxPanel-x.x.x.zip （x.x.x是版本号，刚才下载哪个就输入哪个）
4、切换到升级包目录：cd panel
5、执行升级脚本：bash update.sh
6、删除升级包：cd .. && rm -f LinuxPanel-x.x.x.zip && rm -rf panel
3、简单设置下
为了更安全，你可以执行以下内容，避免一些问题~~

echo '127.0.0.1 bt.cn' >>/etc/hosts
