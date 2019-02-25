# html_css3
html+css3 布局 盒模型
>
#### 三栏布局
- 5种 水平方向的三栏布局
- 4中 垂直方向的三栏布局

#### 盒模型
-  标准模型：width = 内容content 的宽度；(默认）                                                   
   设置方式： box-sizing:content-box;
-  IE模型：width  = 内容content + 边框border + 内边距paddig 的宽度；                  
   设置方式： box-sizing:border-box;

#### js获取盒模型的宽高
-   1.dom.style.width/height                  
    只能获取到dom的内联样式

-   2.dom.currentStyle.width/height        
    获取到的是dom的实际宽高，但这种方式只在IE中可以使用

-   3.window.getComputedStyle(dom,null).width/height                  
    获取到的是dom的实际宽高，但是不支持IE

-   4.dom.offsetWidth/offerHeight                      
    最常用的，兼容性最好的

#### BFC
-   BFC概念：块级格式化上下文
-   BFC的原理：
    BFC的区域不会与浮动区域重叠
    计算BFC区域高度时，浮动区域也参与计算
    BFC区域是独立的一个区域，不与其他区域相互影响
-   如何创建BFC
    脱离文档流：float不为none；position为absolutely或fixed
    overflow不为visible（如overflow：hidden）
    isplay为“table-cell”, “table-caption”,  “inline-block”中的任何一个
-   BFC应用场景
    清除浮动
    防止垂直margin重叠
    自适应两栏布局