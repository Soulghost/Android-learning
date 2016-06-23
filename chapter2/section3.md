# 基本界面组件
####Android系统的界面控件分为定制控件和系统控件
* 定制控件是用户独立开发的控件，或通过继承并修改系统控件后所产生的新控件。能够为用户提供特殊的功能或与众不同的显示需求方式。
* 系统控件是Android系统提供给用户已经封装的界面控件。提供在应用程序开发过程中常见功能控件。系统控件更有利于帮助用户进行快速开发，同时能够使Android系统中应用程序的界面保持一致性。

####常见的系统控件包括
* TextView、EditText、Button、ImageButton、Checkbox、RadioButton、Spinner、ListView和TabHost
#####TextView和EditText
* TextView是一种用于显示字符串的控件
* EditText则是用来输入和编辑字符串的控件，EditText是一个具有编辑功能的TextView

```
 <TextView android:id="@+id/TextView01"
	android:layout_width="wrap_content" 
	android:layout_height="wrap_content"
	android:text="TextView01" >
    </TextView>
    < EditText android:id="@+id/EditText01" 
	android:layout_width="fill_parent" 
	android:layout_height="wrap_content"
	android:text="EditText01" >
    </EditText>

```
（图片）
*第1行android:id属性声明了TextView的ID，这个ID主要用于在代码中引用这个TextView对象*
* “@+id/TextView01”表示所设置的ID值
* @表示后面的字符串是ID资源
* 加号（+）表示需要建立新资源名称，并添加到R.java文件中
* 斜杠后面的字符串（TextView01）表示新资源的名称
* 如果资源不是新添加的，或属于Android框架的ID资源，则不需要使用加号（+），但必须添加Android包的命名空间，例如android:id="@android:id/empty"

*第2行的android:layout_width属性用来设置TextView的宽度，wrap_content表示TextView的宽度只要能够包含所显示的字符串即可*

*第3行的android:layout_height属性用来设置TextView的高度*

*第4行表示TextView所显示的字符串，在后面将通过代码更改TextView的显示内容*
*第7行中“fill_content”表示EditText的宽度将等于父控件的宽度*

```
TextView textView = (TextView)findViewById(R.id.TextView01);
EditText editText = (EditText)findViewById(R.id.EditText01);
textView.setText("用户名：");
editText.setText("");

```
*第1行代码的findViewById()函数能够通过ID引用界面上的任何控件，只要该控件在XML文件中定义过ID即可*

*第3行代码的setText()函数用来设置TextView所显示的内容*




















