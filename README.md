###Adult Download

***

再次重构代码，以达到更抽象，更灵活的代码。

现在也就称得上是个小工具，一个方法入口多线程执行而已，没有良好的可维护和可扩展性。

计划分为以下组件

* Input: 输入组件，可以是网站的页面源码，也可以是本地的页面文件等。

* Process: 处理组件，根据输入信息解析页面，高度灵活。

* Output: 输出组件，可以理解为持久层，如文件形式，数据库形式等。

* Download: 下载组件，通用的，负责下载页面提供给输入组件，下载BT种子文件，图片等。

组件之间的数据流对象

* Request 请求对象，下载页面时必要的请求信息，如URL地址，请求方法，登录用户名和密码等。

* Page 页面对象，请求得到的页面原始信息，交给Process处理。

* PageResult 页面结果对象，Process处理后得到的结果信息，交给Output处理。

***

一个简单的自动化下载小程序，包括图片下载,种子和图片下载两部分。

请勿卵用,哦不是乱用!!!

请勿乱用，请勿乱用，请勿乱用!!!

不要传播,不要传播,不要传播!!!

重要事情说三遍。

欢迎提交Issues(你的任何想法,或想加入的xxx网站,或代码优化,或不合理的代码等等...)

Fork来提交PR吧,骚年...

别叫我老司机,叫我无人机

### 技术

- 完全使用Jsoup请求解析
- typesafe config处理配置文件
- junit测试

目前只支持两个网站。

- xxx图片站,功能是全站多线程下载图片保存磁盘。
- xxx论坛站,功能是登录论坛,请求帖子列表页,多线程解析种子附件下载地址,图片地址,下载保存磁盘。

### 如何使用

- 修改resources目录下的application.conf下的download.path属性,修改为想要的磁盘目录地址

- 运行App,主方法.需要传入参数,p表示下载图片;t表示下载种子和图片


### 计划

- 加入打印日志

- 超时重试处理

- 增加caoliu等论坛