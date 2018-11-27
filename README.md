# RippleEffect
<img src="https://github.com/zhufui/RippleEffect/blob/master/screenshot/1.png" width="720" height="1280"/>

1.系统自带有界水波纹效果

	<Button
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="10dp"
            android:background="?android:attr/selectableItemBackground"
            android:text="系统自带有界水波纹效果" />



2.系统自带有界水波纹效果
系统版本在21以上才能使用，21以下会报错

	<Button
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="10dp"
            android:background="?android:attr/selectableItemBackgroundBorderless"
            android:text="系统自带无界水波纹效果"
            tools:ignore="NewApi" />


3.自定义水波纹效果

	<Button
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="10dp"
            android:background="@drawable/white_ripple"
            android:text="自定义水波纹效果" />

创建一个drawable-v21目录，存放水波纹效果

	<?xml version="1.0" encoding="utf-8"?>
	<ripple xmlns:android="http://schemas.android.com/apk/res/android"
    android:color="@color/_1A000000">
    <item>
        <shape>
            <solid android:color="@color/_FFFFFF"></solid>
        </shape>
    </item>
	</ripple>

在drawable中存放选中效果，不添加的话，在21以下的机器会报错，两个文件的名称要相同

	<?xml version="1.0" encoding="utf-8"?>
	<selector xmlns:android="http://schemas.android.com/apk/res/android">
    	<item android:drawable="@color/_1A000000" android:state_pressed="true" />
    	<item android:drawable="@color/_1A000000" android:state_checked="true" />
    	<item android:drawable="@color/_FFFFFF" />
	</selector>


4.给布局添加水波纹效果

	<LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="10dp"
            android:background="?android:attr/selectableItemBackground"
            android:clickable="true"
            android:focusable="true"
            android:orientation="horizontal">

            <ImageView
                android:id="@+id/iv"
                android:layout_width="50dp"
                android:layout_height="50dp"
                android:src="@mipmap/ic_launcher" />

            <TextView
                android:id="@+id/tv"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_gravity="center_vertical"
                android:text="自定义布局显示水波纹效果" />
        </LinearLayout>

5.按下/抬起状态，背景是纯色

	<?xml version="1.0" encoding="utf-8"?>
	<selector xmlns:android="http://schemas.android.com/apk/res/android">
    	<item android:drawable="@color/_1A000000" android:state_pressed="true" />
    	<item android:drawable="@color/_1A000000" android:state_checked="true" />
    	<item android:drawable="@color/_FFFFFF" />
	</selector>


6.按下/抬起状态，带阴影的圆角背景

	<Button
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="10dp"
            android:background="@drawable/sel_coner_bg"
            android:text="带阴影的圆角背景" />

xml文件中的写法：

	<?xml version="1.0" encoding="utf-8"?>
	<selector xmlns:android="http://schemas.android.com/apk/res/android">
    	<item android:drawable="@drawable/shape_dialog_f4f3f4" android:state_pressed="true" />
    	<item android:drawable="@drawable/shape_dialog_f4f3f4" android:state_focused="true" />
    	<item android:drawable="@drawable/shape_dialog_withe" />
	</selector>


7.按下/抬起状态，不带阴影的圆角背景
这比上面的就多了一个style的属性

	<Button
            style="?android:attr/borderlessButtonStyle"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="10dp"
            android:background="@drawable/sel_coner_bg"
            android:text="不带阴影的圆角背景" />

8.圆形渐变

	<TextView
            android:layout_width="50dp"
            android:layout_height="50dp"
            android:layout_gravity="center_horizontal"
            android:layout_margin="10dp"
            android:background="@drawable/shape_circle_bg"
            android:gravity="center"
            android:text="圆形渐变"
            android:textSize="12sp" />

xml文件中的写法：

	<?xml version="1.0" encoding="utf-8"?>
	<shape xmlns:android="http://schemas.android.com/apk/res/android"
    	android:shape="oval">
    	<size
    	    android:width="24dp"
    	    android:height="24dp" />
    	<gradient
    	    android:angle="90"
    	    android:endColor="@color/_FE8D42"
    	    android:startColor="@color/_FEB242" />
	</shape>


9.水平椭圆形背景

	<Button
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="10dp"
            android:background="@drawable/shape_oval_bg"
            android:text="水平椭圆形背景" />

xml文件中的写法：

	<?xml version="1.0" encoding="utf-8"?>
	<shape xmlns:android="http://schemas.android.com/apk/res/android">
    	<solid android:color="#FA6E6E " />
    	<corners android:radius="9999dp" />
	</shape>

10.竖直椭圆形背景

	<Button
            android:layout_width="20dp"
            android:layout_height="100dp"
            android:layout_gravity="center_horizontal"
            android:layout_margin="10dp"
            android:background="@drawable/shape_oval_bg"
            android:text="竖直椭圆形背景"
            android:textSize="12sp" />

11.带边框的背景

	<Button
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="10dp"
            android:background="@drawable/shape_line_bg"
            android:text="带边框的背景" />

xml文件中的写法：

	<?xml version="1.0" encoding="utf-8"?>
	<shape xmlns:android="http://schemas.android.com/apk/res/android">
    	<solid android:color="@color/_D8D8D8" />
    	<stroke
    	    android:width="1.5dp"
    	    android:color="@color/_FA6E6E" />
	</shape>

12.渐变圆角背景

	<Button
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="10dp"
            android:background="@drawable/shape_radius_shade"
            android:text="渐变圆角背景" />

xml文件中的写法：

	<?xml version="1.0" encoding="utf-8"?>
	<shape xmlns:android="http://schemas.android.com/apk/res/android">
    	<gradient
    	    android:angle="90"
    	    android:endColor="@color/_FA8C64"
    	    android:startColor="@color/_FA5F5F" />
    	<corners android:radius="12dp" />
	</shape>


13.选中/未选中,背景是图片

	<ImageButton
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center_horizontal"
            android:layout_margin="10dp"
            android:background="@drawable/sel_search" />

xml文件中的写法：

	<?xml version="1.0" encoding="utf-8"?>
	<selector xmlns:android="http://schemas.android.com/apk/res/android">
    	<item android:drawable="@drawable/im_search_pressed" android:state_pressed="true" />
    	<item android:drawable="@drawable/im_search_normal" />
	</selector>




