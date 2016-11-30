---
layout: default
title: Github Blog添加评论功能（多说）
---
这两天在玩github blog 索性看了下为github添加评论功能，搜了下发现有个不错的社会化评论系统“[多说](http://duoshuo.com/ "多说")”http://duoshuo.com/ ，而且不少github blog主都使用了这个评论系统。

废话不多少说，其实“多少”已经将对接做的很简单了：

1. 访问多说http://duoshuo.com/ 官网点击我要安装，使用个微博、qq之类的社交帐号授权下，完成后会出现“创建站点”，在“站点地址”栏处填入blog域名，如“http://blog.heytobye.com”, 完成后会出现示例代码。

2. 复制粘帖至github blog的模板页“default.html”的<body></body>之间，我的blog套用了Jekyll语法，所以配置为：
{% highlight html %}
<div class="ds-thread" 
	data-thread-key="/2016/11/28/hello-github-blog.html"
	data-title="Github Blog添加评论功能（多说）"
	data-url="http://yourblogdomain/2016/11/28/hello-github-blog.html">
</div>
{% endhighlight %}
{% highlight js %}
<script type="text/javascript">
var duoshuoQuery = {short_name:"heytobye"};
	(function() {
		var ds = document.createElement('script');
		ds.type = 'text/javascript';ds.async = true;
		ds.src = (document.location.protocol == 'https:' ? 'https:' : 'http:') + '//static.duoshuo.com/embed.js';
		ds.charset = 'UTF-8';
		(document.getElementsByTagName('head')[0] 
		 || document.getElementsByTagName('body')[0]).appendChild(ds);
	})();
</script>
{% endhighlight %}

当然你可以将<sctript></sctript>添加至你的JS文件内。

3. commit下，push下，就算完成了，其它人说要等10分钟，其实我这感觉push成功就完事了。

致谢：“[多说](http://duoshuo.com "多说")”