# luci-app-v2ray

声明我只是个新手,有问题请留言.这是一个存档备份

具体源码来源看下面两个链接:

1.本app从https://github.com/coolsnowwolf/lede/pull/331 中提取

2.由https://github.com/Dango233/lede/commit/ed30d79ae1653df05e09c28fea330d325394797f 优化

3.简单使用说明
在服务器设置中,使用配置文件-配置文件类型为JSON时,需确保

	"inbound": {
		"port": 7070,
		"protocol": "dokodemo-door",
		"settings": {
			"followRedirect": true,
				"timeout": 30
					},
		"domainOverride": ["tls", "http"]
  },



	"dns": {
	"servers": [
		"8.8.8.8",
		"8.8.4.4",
		"localhost"
		]
	},
    
inbound  dns 为以上配置方可正常透明代理.
