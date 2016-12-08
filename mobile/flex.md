# flex 弹性布局盒模型
## 设置弹性盒模型
  1.display:flex(新版)
  2 display:-webkit-box(旧版)
## flex容器
  1. 项目排列的方向
     1.1 row 从左到右排列（默认的）
     1.2 row-reverse 从左到右
     1.3 column 从上到下
     1.4 column-reverse 从下到上
  <code>flex-direction:row | row-reverse | column | column-reverse </code>
     + horizontal 水平方式
     + vertical 垂直方向
       -wibkit-box-orient:horizontal | vertical
     + normal 顺序正常
     + reverse 反向
       -wibkit-box-direction:normal | reverse
  2. 项目包裹方式
     2.1 nowrap 不换行（默认）
     2.2 wrap   容器如果不足以放下项目，自动换行到下一行
     2.3 wrap-reserve 容器如果不足以放下项目，自动换行到上一行
     
      <code>  flex-wrap:nowrap | wrap | wrap-reserve</code>
  3. 项目水平对齐方式
     3.1 flex-start 左对齐
     3.2 flex-end 右对齐
     3.3 center   居中
     3.4 space-between 两端对齐
     3.5 space-around  每个项目两侧的间隔相等
      
     <code>  justify-content:flex-start | flex-end | center | space-between | space0around</code>
     
      - start 左对齐
      - end   右对齐
      - center 居中
      - justify 两端对齐
      <code> -webkit-box-pack:start | end | center| justify
  4.  项目的垂直对齐方式
     4.1 flex-start  顶对齐
     4.2 flex-end  底对齐
     4.3 center  垂直居中
     4.4 baseline 以项目的第一行文字的基线对齐
     4.5 sretch 如果项目容未设置高度，占满整个容器高度
      
       <code> align-items:flex-start | flex-end | center | baseline | sretch </code>
       
       - start 顶对齐
       - end   底对齐
       - center 垂直居中
       <code> -webkit-box-align:start | end | center  </code>
  
  5. 多行对齐方式
     5.1 flex-start 左对齐
     5.2 flex-end 右对齐
     5.3 center 中对齐
     5.4 space-between 两端对齐
     5.5 space-around 每个项目距离相同
     5.6 stretch 沾满容器高度（拉升）
     
      <code> align-content:flex-start | flex-end | center |space-between | space-around |  stretch <code>
      
## flex 项目（列表）
  1. 项目排序
     1.1 项目的排序，数字越小越靠前，默认值为0，接收负值
     
     order:<init>

       - 项目的排序，数字越小越靠前，默认值为1，将0 或负数转为1
       <code> -webkit-box-ordinal-group <code>
       
  2. 项目占比（放大）
     2.1 所占栅格比例默认为0 项目的尺寸=容器的尺寸/总栅格数*当前栅格数
     
      <code> flex-grow: <int>
      
      - 老版弹性布局设置项目栅格
       <code> -webkit-box-flex:<int> </code>
        
  3. 项目占比（缩小）
     3.1 所占栅格比例默认为1
     
       <code> flex-shrink:<int> </code>
       
  4. 所占项目空间大小
      4.1 可以设置项目的大小 类似于width\height属性
      
      <code> flex-basis:<size> | auto
      
  5. 项目自己的对齐方式 优先级高于容器的 align-items 
  
     <code>align-self: auto | flex-start | flex-end | center | baseline | stretch</code>
       