# html

## 标签

* head 

* body

* link 表示链接外部样式表

* meta 不显示在网页上，只能在源代码中看到

* div 将网页内容分成区域

* section 定义文章中的节，比如章节、页眉、页脚或文章中的其他部分

* header 定义文档或者文档的一部分区域的页眉

* abbr 可以表示缩写的英语词语

* map

  * 不是地图标签，事映射标签
  * 如果设置了id属性的话，必须与name属性的值一样

* area

  * 必须作为map的子元素

  * href target alt 三个属性与a标签用法一样

  * shape （rect矩形  circle圆形 poly多边形）

  * coords 对应shape几种图形的坐标

  * <img src="" usemap="#somemap" alt="">

    ​           <map name="somemap">

    ​            <area shape="rect" coords="55,108,205,200" href="https://www.mi.com/" alt="ieksoef" title="abc" target="_blank">

    ​            <area shape="circle" coords="133,262,90" href="" alt="">

    ​            <area shape="poly" coords="57,82,8,265,163,397,225,256,187,83" href="" alt="">

    ​           </map>

* iframe 内嵌框架

  * 必须有开始与结束标签

  * 可以在标签之间写上不支持此标签的退化内容

  * 各种属性

    * src

    * name (自定义名字)

      提及a标签的target属性（_self, _blank,  _top, _parent ）

      

* * 它的跳转后退也会存在于浏览器的前进后退的记录里面

* frameset/frame

  * <frameset rows="100px,*,100px">

    ​          <frame src="https://www.jd.com/"> 

    ​          <frameset cols="50,50">

    ​           <frame src="https://www.jd.com/">

    ​           <frame src="https://www.jd.com/">

    ​          </frameset>

    ​          <frame src="https://xieranmaya.github.io/">

    ​         </frameset>

* 标签的退化方案 <iframe>your  brower dont support iframe</iframe>,

  

  ​                            <frameset>

  ​                              	<frame src="">

  ​                            </frameset>

  ​                            <noframeset>your  brower dont support  frameset</frameset>,

  

  ​                             <canva><p>no supported</p> </canvas>,

  

  ​                             <script> var a = 8  </script>

            <noscript>your browser dont support javascript!</noscript>

  ​         fallback 退化方案

  ​         degrade 降级方案

  ​         backdrop 备用方案

### 表单标签

* form  

  * action 表单提交的地址
  * target 与a标签类似，打开新的窗口

* input

  * type属性的各项值

    * text 文本
    * password 密码
    * checkbox 复选框 （以name相同分组  checked属性表示默认选中）
    * radio 单选框（剩余同上）
    * button 按钮
    * submit 提交 
    * number
    * file 文件
      1. accept 接受文件类型

    * date
    * color
    * range
    * month
    * week
    * time
    * datetime
    * datetime-local
    * email
    * tel
    * url

* input

  * value
  * 为按钮形态时，设置上面的文字
    * 为输入框时，设置里面的默认内容
  * disabled
    * 无值的属性
    * 禁用这个输入域
  * required
    * 设置这个输入域为必填项
    * 不填的话，则无法用正常手段提交
  * maxlength
    * 为文本输入框时，设置输入的最大长度
  * minlength
    * 为文本输入框时，设置输入的最小长度
    * 不过兼容性不太好，不少浏览器没有实现

  * placeholder
    * 提示文本框内该输入相关的信息
  * autofocus
    * 自动获得焦点，即页面加载完后光标自动在这个元素内
  * tabindex
    * 按tab键在不同输入域之间跳转时的顺序
    * 会往顺序更大的元素跳，为-1的话会跳过该元素
  * name
    * 表单提交时，这个域/字段/框的名字
    * 在radio和checkbox阵列里，name相同的元素被分在同一组

* button

  * type属性

    * 不写type属性的话，默认为submit

      即：点击默认为submit

    * button 常规按钮， submit 提交按钮， reset 重置按钮

  * 与<input type="button" name="b" value="123">区别

    * input的button只能在按钮上显示纯文字
    * 而button标签可以在按钮上显示其他内容如：图片（嵌套其他标签），文字也可以设置不同颜色

    


* label

  * 一般与checkbox及radio一起用，以扩大这两个按钮的可点击区域，比较典型的是与input：file一起用

  * for 

    * 为想要被扩大点击区域的id <label for="one">123</label>
    * ​                                                   <input type="text" id="one">
    * 表单元素嵌套在label时不用for属性 <label> <input type="checkbox”> 男</label>

    

* select

  * 下拉选择框
  * 属性
    * multiple  无属性值，表示多选，多选时就不是下拉样式了

* option

  * value 选择了该项目后它所属的select元素的name值
  * selected 默认被选中 (无属性值)
  * disabled 表示该项被禁用 （无属性值）
  * hidden 表示该项被隐藏 （无属性值）

* optgroup/hgroup/colgroup  给option分组，用label属性表示这个分组的名字，有一个disabled属性，如果设置这个属性，整组标签都会被禁用

* fieldset 

  * 这个标签是用来给输入域分组的
  * fieldset有一个disabled属性，如果它有这个属性，其内的所有输入域都将被禁用

* legend

* 只能作为fieldest的子元素用来标识这组输入域的名字，基本上没有其它用处

* table

* caption  表格标题

* thead 表头

* tobody 表格主体

* tfoot 表尾

* tr 表格行

* th 用在表头单元格，表示文字加粗

* td 表示数据单元格

* colspan 跨列

* rowspan 跨行

* colgroup

  * 可以用来分组
  * span属性，表示选择多列

* col

  * 用来设置表格列的属性和样式
  * span属性，表示选择多少列表格
  * col/colgroup 必须出现在caption后面，thead/tbody的前面

* cellspacing=0

* tr或者td or th不能有其它并列标签,否则会识别错误



## git

* git init 在一个文件夹的.git文件夹下初始化一个仓库
* git status 查看当前仓库状态
* git add file.txt 添加file.txt到待提交区5
* git commit -m “提交信息”
* git diff 显示被跟踪的文件的修改状态
* git log 查看提交日志/历史
* git remote add origin  https://github.com/lizhaolu111/learn-git.git  在githup上面创建一个仓库
* git push -u origin master 将本地与远程关联

 