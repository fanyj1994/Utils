# 常用的前端工具代码

### 清除浮动
``` CSS
.clearfix::after {
  content: "";
  display: block;
  clear: both;
}
```

> 关于其它清除浮动的方法及缺点，主要有：
 - 在要清除浮动的元素后面添加额外标签，并 `clear: both;`，缺点：会添加额外标记，语义不友好；
 - 为父元素设置 `overflow: hidden;`, 触发 BFC,缺点：可能会使得内容被隐藏，并且使鼠标中键失灵；
 - 为父元素设置 float 属性，触发 BFC, 缺点：影响与父元素相邻的元素；
 - 为父元素设置 `display: table;`, 缺点：改变盒模型属性
 
### 一行文本过长截断处理，并显示...截断符号`
``` CSS
text-overflow: hidden;
white-space: nowrap;
text-overflow: ellipsis;
width: 200px;
```