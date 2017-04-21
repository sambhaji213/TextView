# TextView
A TextView displays text to the user and optionally allows them to edit it. A TextView is a complete text editor, however the basic class is configured to not allow editing.

**TextView Attributes**
Following are the important attributes related to TextView control. You can check Android official documentation for complete list of attributes and related methods which you can use to change these attributes are run time.

Sr.No.	| Attribute & Description
------------ | -------------
1	| <b>android:id </b><br>This is the ID which uniquely identifies the control.
2	| <b>android:capitalize</b><br> If set, specifies that this TextView has a textual input method and should automatically capitalize 
3	| <b>android:cursorVisible</b><br> Makes the cursor visible (the default) or invisible. Default is false.
4	| <b>android:editable</b><br> If set to true, specifies that this TextView has an input method.
5	| <b>android:fontFamily</b><br> Font family (named by string) for the text.
6	| <b>android:gravity</b><br> Specifies how to align the text by the view's x- and/or y-axis when the text is smaller than the view.
7	| <b>android:hint</b><br> Hint text to display when the text is empty.
8	| <b>android:inputType</b><br> The type of data being placed in a text field. Phone, Date, Time, Number, Password etc.
9	| <b>android:maxHeight</b><br> Makes the TextView be at most this many pixels tall.
10	| <b>android:maxWidth</b><br> Makes the TextView be at most this many pixels wide.
11	| <b>android:minHeightv Makes the TextView be at least this many pixels tall.
12	| <b>android:minWidth</b><br> Makes the TextView be at least this many pixels wide.
13	| <b>android:password</b><br> Whether the characters of the field are displayed as password dots instead of themselves. Possible value either "true" or "false".
14	| <b>android:phoneNumber</b><br> If set, specifies that this TextView has a phone number input method. Possible value either "true" or "false".
15	| <b>android:text</b><br> Text to display.
16	| <b>android:textAllCaps</b><br> Present the text in ALL CAPS. Possible value either "true" or "false".
17	| <b>android:textColorText</b><br> color. May be a color value, in the form of "#rgb", "#argb", "#rrggbb", or "#aarrggbb".
18	| <b>android:textColorHighlight</b><br> Color of the text selection highlight.
19	| <b>android:textColorHintv Color of the hint text. May be a color value, in the form of "#rgb", "#argb", "#rrggbb", or "#aarrggbb".
20	| <b>android:textIsSelectable</b><br> Indicates that the content of a non-editable text can be selected. Possible value either "true" or "false".
21	| <b>android:textSize</b><br> Size of the text. Recommended dimension type for text is "sp" for scaled-pixels (example: 15sp).
22	| <b>android:textStyleStyle</b><br> (bold, italic, bolditalic) for the text. You can use or more of the following values separated by '|'.
23	| <b>android:typeface</b><br> Typeface (normal, sans, serif, monospace) for the text. You can use or more of the following values separated by '|'.

**activity_main**
```
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@android:color/white"
    android:padding="16dp"
    tools:context=".MainActivity" >

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_centerInParent="true"
        android:gravity="center"
        android:text="My TextView"
        android:textColor="@color/colorAccent"
        android:textSize="50sp"/>

</RelativeLayout>
```

**MainActivity**
```
package com.sambhaji.textview;

import android.os.Bundle;
import android.support.design.widget.FloatingActionButton;
import android.support.design.widget.Snackbar;
import android.support.v7.app.AppCompatActivity;
import android.support.v7.widget.Toolbar;
import android.view.View;
import android.view.Menu;
import android.view.MenuItem;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

    }

    @Override
    public boolean onCreateOptionsMenu(Menu menu) {
        // Inflate the menu; this adds items to the action bar if it is present.
        getMenuInflater().inflate(R.menu.menu_main, menu);
        return true;
    }

    @Override
    public boolean onOptionsItemSelected(MenuItem item) {
        // Handle action bar item clicks here. The action bar will
        // automatically handle clicks on the Home/Up button, so long
        // as you specify a parent activity in AndroidManifest.xml.
        int id = item.getItemId();

        //noinspection SimplifiableIfStatement
        if (id == R.id.action_settings) {
            return true;
        }

        return super.onOptionsItemSelected(item);
    }
}
```
<a href="url"><img src="https://github.com/sambhaji213/TextView/blob/master/screenshot/home.png" align="left" height="480" width="250"></a>
