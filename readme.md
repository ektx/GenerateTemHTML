# GenerateTemHTML
HTML模板生成器  

## 参数说明
```js
	@temlpate: 模板名称，最好是id,样式最好是唯一
	@data: JSON数组数据
```

## 使用方式：
将要使用的HTML指定一个id,对内容数据进行[[[数据可以用内容]]]来处理  
```html
<head>
...
<!-- 添加 jq -->
<script src="js/jquery.min.js"></script>
<!-- 添加 generateTemHTML -->
<script src="js/generateTemHTML.js"></script>
...
</head>
<body>
	<!-- 编写模板 -->
	<ul id="demo-template">
		<li>
			<h2>[[[姓名]]]</h2>
			<p>[[[年龄]]]</p>
		</li>
	</ul>

<script>
	var data =  [
		{'姓名': 'zwl', '年龄': 27},
		{'姓名': '张飞', '年龄': 57}
	];

	// 引入模板
	var html = generateTemHTML('#demo-template', data)
	// 生成代码
	$('#demo-template').html(html)
</script>
</body>
```