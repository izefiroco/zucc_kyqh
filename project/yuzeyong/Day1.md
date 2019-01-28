第一天接触前端,感觉一头雾水,对介绍里的语言框架之前没有任何了解,在此摘部分还未理解的地方,以及自己的理解
##HTML和CSS
HTML是一种标记语言,拿来添加一些富文本内容
再配上CSS来规定样式之后网页看着就比较正常了
>CSS基本格式:
>属性:值
>比如说 position:fixed,位置不动的意思
>
>left:0px
>top:0px
>代表紧贴窗口左上角

HTML5就是其中一个比较新的标准。这个标准新加了很多可以用的标签和属性,本来前端程序员要写一堆代码去实现的效果，现在浏览器都给你实现好了，只要写两三行，调用一下浏览器给你实现的部分就能搞定，简单愉快.

##JavaScript与浏览器脚本
网站的一些动态效果需要脚本来实现,现在的标准就是用JS

##PHP,服务器脚本
Web Service传输的数据主要由服务器脚本生成(同一个网址,每个人看到的页面是不一样的)

##综上:HTML是名词,CSS是形容词,JavaScript是动词

#一个小型网站访问的过程
1:用户操作浏览器访问，浏览器向服务器发出一个 HTTP 请求；
2:服务器接收到 HTTP 请求，Web Server 进行相应的初步处理，使用服务器脚本生成页面；
3:服务器脚本（利用Web Framework）调用本地和客户端传来的数据，生成页面；
4:Web Server 将生成的页面作为 HTTP 响应的 body，根据不同的处理结果生成 HTTP header，发回给客户端；
5:客户端（浏览器）接收到 HTTP 响应，通常第一个请求得到的 HTTP 响应的 body 里是 HTML 代码，于是对 HTML 代码开始解析；
6:解析过程中遇到引用的服务器上的资源（额外的 CSS、JS代码，图片、音视频，附件等），再向 Web Server 发送请求，Web Server 找到对应的文件，发送回来；
7:浏览器解析 HTML 包含的内容，用得到的 CSS 代码进行外观上的进一步渲染，JS 代码也可能会对外观进行一定的处理；
8:用户与页面交互（点击，悬停等等）时，JS 代码对此作出一定的反应，添加特效与动画；
9:交互的过程中可能需要向服务器索取或提交额外的数据（局部的刷新，类似微博的新消息通知），一般不是跳转就是通过 JS 代码（响应某个动作或者定时）向 Web Server 发送请求，Web Server 再用服务器脚本进行处理（生成资源or写入数据之类的），把资源返回给客户端，客户端用得到的资源来实现动态效果或其他改变。