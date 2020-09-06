# linux-notes

## linux启动

- 运行init，需读取配置文件/etc/inittab
- 第一级别：表单用户模式
- 第二级别：多用户模式，不带网络配置
- 第三级别：多用户模式,带网络配置

## 远程登陆liunx

- 确定网卡是否激活

> root账户登录，输入ifconfig
> 如果eth0设备没有inet addr(IP地址)
> 使用以下命令：ifup eth0(检查eth0是否已启动)

- 确定防火墙规则

> service iptables status  
> 如果没有22默认端口，需要手动添加：iptables -A INPUT -P tcp --dport 22 -j ACCEPT

- 如果想修改启动端口

> 可以更改ssh服务的配置文件(/etc/ssh/sshd_config)
