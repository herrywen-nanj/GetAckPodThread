# 背景
#### 在阿里云ACK中部署了单体spring boot应用，但是当cpu使用率大于90%时，应用会出现问题，为了拿到问题pod中的jvm dump文件便于开发人员分析和解决由于cpu过高引起的服务问题

# 功能
#### 1.依赖阿里云ARMS接口的prometheus提供的监控CPU数据，默认检查5次，远程获取CPU使用大于90%的ACK中的POD名称
#### 2.将问题POD中的线程堆栈日志文件，自动拷贝至FTP对应目录下,便于分析
#### 3.重启对应POD

# 使用方法
#### 在test.conf中配置对应内容，并将main.sh作为计划任务


