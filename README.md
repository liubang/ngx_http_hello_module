# ngx_http_hello_module

这是nginx模块开发的示例代码，开启nginx源码研究的大门！

## 安装

下载最新的nginx源码

```shell
cd nginx_path
./auto/configure --prefix=/opt/app/nginx_dev --add-module=../ngx_http_hello_module
make && sudo make install
```

修改nginx配置文件

```conf
server {
        listen       80;
        server_name  localhost;

	location /test {
		hello_string liubang;
        hello_counter on;
	}
}
```

测试，访问浏览器`http://localhost/test`

参考文档：[http://tengine.taobao.org/book/chapter_03.html#hello-handler](http://tengine.taobao.org/book/chapter_03.html#hello-handler)
