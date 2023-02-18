引用两个文件

在js文件中加入

```js
 //图片灯箱开始
 $(function() {
     //定义哪个元素中的img
 	$(".card-img  img").each(function() {
 		if (!this.parentNode.href) {
 			$(this).wrap("<a href='" + this.src + "' data-fancybox='fancybox' data-caption='" + this.alt + "'></a>")
 		}
 	})
 });
//没设置一个元素都要添加以下代码
 $(document).ready(function() {
 	$("[data-fancybox]").fancybox()
 });
 //图片灯箱结束
```

