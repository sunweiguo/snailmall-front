# snailmall-front
快乐蜗牛商城配套的前端代码


## 项目初始化步骤

1.安装nodejs环境,推荐使用v4.4.7
    下载地址 : https://nodejs.org/download/release/v4.4.7/

2.全局安装webpack v^1.15.0
    命令: (sudo) npm install -g webpack@^1.15.0

3.全局安装webpack-dev-server v^1.16.5
    命令: (sudo) npm install -g webpack-dev-server@^1.16.5

4.在项目根目录执行npm初始化
    命令: npm install (--registry=https://registry.npm.taobao.org)

5.对于前端项目，到webpack.config.js文件中，要注意这段代码：

```
output: {
    path        : __dirname + '/dist/',
    publicPath : 'dev' === WEBPACK_ENV ? '//s.oursnail.cn/snailmall_fe/dist/' : '//s.oursnail.cn/snailmall_fe/dist/',
    filename    : 'js/[name].js'
}
```

指向自己指定的静态文件域名。

还有就是如果要修改前端的背景图，到`/page/common`目录找到`layout.css`:

```
body{
    background: #f6f6f6;
    font: 12px/1.5 tahoma, arial, Microsoft YaHei, sans-serif;
    background-image:url('http://bloghello.oursnail.cn/feather.jpg');
}
```