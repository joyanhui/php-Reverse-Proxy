# php反向代理

## 基本目标

镜像站点，并输出，用于替代nginx的反向代理

## 已经实现

全站的反代

header跟随跳转

cookies的基本适配

## 计划中
缓存的建立更新、删除

cookies和session的同步等功能的实现

ip地址的穿透

简单的字符串替换等

基于url规则的缓存方案

可视化的管理后台

### 注意
完全是基于虚拟主机的环境来实现php的反向代理，因廉价虚拟机主机的特性以及限制。

所以无法使用多线程等特性。

redis memcache等内存加速等均不在优先考虑范围之内。

因廉价虚拟主机特性是空间大而mysql数据库小，所以优先基于文件的缓存或文件性数据库。

sqlite在大并发读取下性能并不差，在写入的时候因为存在文件锁的问题所以未来会采取读写分离的方法来缓存。
