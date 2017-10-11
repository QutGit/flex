# Flex 布局

参考地址：

语法：http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html
实例：http://www.ruanyifeng.com/blog/2015/07/flex-examples.html


1.布局 传统解决方案
  基于盒状模型，依赖 display 属性 + position 属性 + float 属性
  缺点：对于那些特殊布局非常不用一实现，比如垂直居中

2.2009年W3C提出了一种新的方案---flex布局，可以简便，完整，响应式的实现各种页面布局
  只是针对网页布局（layout）

3.Flex 是Flexible Box的缩写，意为：弹性布局，用来为盒状模型提供最大的灵活性
  任何一个容器都可以指定为Flex布局
  行内元素也可以用flex布局

注：设为flex布局以后，子元素的float、clear、vertical-align属性将失效

4.采用flex布局的元素称为flex 容器，他的所有子元素自从成为容器成员，称为flex项

5.容器默认存在两根轴：水平的主轴（main axis）和垂直的交叉轴（cross axis），flex项默认沿主轴排列

6.容器的属性（设置在容器上）
  flex-direction：决定主轴的方向（flex项的排列方向）：沿主轴或者交叉轴排列
  flex-wrap:默认情况下，flex项都排在一条直线上，flex-wrap属性定义，如果一条轴线排不下如何换行
  flex-flow：是flex-direction属性和 flex-wrap属性的简写形势，默认值为 row nowrap
  justify-content ：定义了flex项在主轴上的对齐方式
  align-items:定义项目在交叉轴上如何对齐
  align-content:定义了多跟轴线的对齐方式，如果项目只有一根轴线，该属性不起作用

7.flex项属性（设置在flex项上）
  order: 定义flex项排列顺序，数值越小，排列越靠前，默认为0
  flex-grow:定义flex项的放大比例，默认为0，即，如果存在剩余空间也不放大
  flex-shrink:定义了flex项的缩小比例，默认为1，即，如果空间不足，该flex项将缩小
  flex-basis:定义了在分配多余空间之前，flex项占据主轴空间。浏览器根据这个属性，计算主轴是否有多余空间，默认值为auto，即flex项本来大小
  flex:是 flex-grow，flex-shrink，flex-basis的简写，默认值为 0 1 auto，后两者的属性可选，该属性有两个快捷值：auto(1 1 auto) 和 none(0 0 auto)
       建议优先使用这个属性，而不是单独写三个分离的属性，因为浏览器会推算相关值
  align-self:属性允许单个flex项有与其他flex项有不一样的对齐方式，可覆盖align-items属性。默认值为auto，
             表示继承父元素的align-items属性，如果没有父元素则等同于stretch


