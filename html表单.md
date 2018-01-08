# html表单 用于搜集不同类型的用户输入

#### form元素  

#####  语法格式

```
HTML 表单用于收集用户输入
<form>
 .
form elements
 .
</form>
```

##### form属性的列表

|       属性       |                    描述                    |
| :------------: | :--------------------------------------: |
| accept-charset |        规定在被提交表单中使用的字符集（默认：页面字符集）。        |
|     action     | 规定向何处提交表单的地址(URL)(提交页面),即定义提交变淡时执行的动作.如果省略action属性,则action会被设置为当前页面 |
|  autocomplete  |          规定浏览器应该自动完成表单（默认：开启）。           |
|    enctype     |       规定被提交数据的编码（默认：url-encoded）。        |
|     method     |       规定在提交表单时所用的 HTTP 方法（默认：GET）。       |
|      name      | 规定识别表单的名称（对于 DOM 使用：document.forms.name）。 |
|   novalidate   |             规定浏览器不验证表单,h5新增              |
|     target     |      规定 action 属性中地址的目标（默认：_self）。       |

#### input元素  最重要的表单元素

##### input的属性
|       类型       |                    描述                    |
| :------------: | :--------------------------------------: |
|      type      |       输入类型,text,password,submite等        |
|     value      |                规定输入字段的初始值                |
|    readonly    | 规定输入字段为只读(不能修改),readonly属性不需要值.它等同于readonly="readonly" |
|    disabled    | 规定输入字段是禁用的,被禁用的元素是不可用和不可点击的,被禁用的元素不会被提交,disabled属性不需要值.它等同于disabled="disabled" |
|      size      |             规定输入字段的尺寸(以字符计)              |
|   maxlength    | 规定输入字段允许的最大长度,如设置 maxlength属性,则输入控件不会接受超过所允许数的字符.该属性不会提供任何反馈。如果需要提醒用户,则必须编写JavaScript代码 |
|  autocomplete  | 表单或输入字段是否应该自动完成,当自动完成开启,浏览器会基于用户之前的输入值自动填写值,可以把表单的autocomplete设置为on,同时把特定的输入字段设置为 off,反之亦然.autocomplete属性适用于form以及如下input类型:text、search、url、tel、email、password、datepickers、range以及color。h5新增 |
|   autofocus    | autofocus是是布尔属性,如果设置,则规定当页面加载时input>元素应该自动获得焦点 |
|      form      | 规定input元素所属的一个或多个表单,如需引用一个以上的表单,请使用空格分隔的表单id列表(输入字段可能位于HTML表单之外,但仍属表单) |
|   formaction   | 规定当提交表单时处理该输入控件的文件的URL,formaction属性覆盖form元素的action属性,formaction属性适用于type="submit"以及type="image" |
|  formenctype   | 规定当把表单数据(form-data)提交至服务器时如何对其进行编码(仅针对method="post"的表单),formenctype属性覆盖form元素的enctype 属性,formenctype 属性适用于type="submit" 以及 type="image" |
|   formmethod   | 定义用以向action UR 发送表单数据(form-data)的HTTP方法,formmethod覆盖form元素的method 属性,formmethod属性适用于type="submit" 以及 type="image" |
| formnovalidate | 是布尔属性,如果设置,则规定在提交表单时不对 input>元素进行验证,formnovalidate 属性覆盖form元素的 novalidate 属性.formnovalidate 属性可用于 type="submit" |
|   formtarget   | 规定的名称或关键词指示提交表单后在何处显示接收到的响应,formtarget 属性会覆盖form>元素的 target 属性。formtarget 属性可与type="submit" 和 type="image" 使用 |
| height 和 width | height 和 width 属性规定input元素的高度和宽度。height 和 width 属性仅用于input type="image" |
|      list      |   list属性引用的datalist元素中包含input元素的预定义选项    |
|   min和max属性    | 规定input元素的最小值和最大值,min 和 max 属性适用于如需输入类型：number、range、date、datetime、datetime-local、month、time 以及 week |
|    multiple    | multiple 属性是布尔属性.如果设置，则规定允许用户在input 元素中输入一个以上的值。multiple 属性适用于以下输入类型:email 和 file |
|    pattern     | pattern属性规定用于检查input>元素值的正则表达式。pattern 属性适用于以下输入类型:text、search、url、tel、email、and password |
|  placeholder   | 规定用以描述输入字段预期值的提示(样本值或有关格式的简短描述),该提示会在用户输入值之前显示在输入字段中.placeholder 属性适用于以下输入类型：text、search、url、tel、email 以及 password |
|    required    | 是布尔属性,如果设置,则规定在提交表单之前必须填写输入字段。required 属性适用于以下输入类型：text、search、url、tel、email、password、date pickers、number、checkbox、radio、and file. |
|      step      | 规定input元素的合法数字间隔,step 属性可与 max 以及 min 属性一同使用，来创建合法值的范围。 |
|      name      |      如果要正确地被提交，每个输入字段必须设置一个 name 属性      |

##### input元素的输入类型,即type的取值
|      输入类型      |                    描述                    |
| :------------: | :--------------------------------------: |
|      text      |              定义供文本输入的单行输入字段              |
|    password    |                  定义密码字段                  |
|     submit     |            定义提交表单数据至表单处理程序的按钮            |
|     radio      |                  定义单选按钮                  |
|    checkbox    |     定义复选框,复选框允许用户在有限数量的选项中选择零个或多个选项      |
|     button     |                   定义按钮                   |
|     number     |         用于应该包含数字值的输入字段,能够对数字做出限制         |
|      date      |              用于应该包含日期的输入字段               |
|     color      |              用于应该包含颜色的输入字段。              |
|     range      | 用于应该包含一定范围内的值的输入字段。能够使用如下属性来规定限制：min、max、step、value |
|     month      |    允许用户选择月份和年份。根据浏览器支持，日期选择器会出现输入字段中。    |
|      week      |     允许用户选择周和年。根据浏览器支持，日期选择器会出现输入字段中      |
|      time      |   允许用户选择时间（无时区）。根据浏览器支持，时间选择器会出现输入字段中    |
|    datetime    |  允许用户选择日期和时间（有时区）。根据浏览器支持，日期选择器会出现输入字段中  |
| datetime-local |             允许用户选择日期和时间（无时区）             |
|     email      |            用于应该包含电子邮件地址的输入字段             |
|     search     |         用于搜索字段（搜索字段的表现类似常规文本字段）          |
|      tel       |             用于应该包含电话号码的输入字段              |
|      url       |            用于应该包含 URL 地址的输入字段            |
#### fieldset元素

```
<fieldset> 元素组合表单中的相关数据
<legend> 元素为 <fieldset> 元素定义标题。
```

