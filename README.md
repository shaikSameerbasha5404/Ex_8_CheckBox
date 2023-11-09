# Ex_8_CheckBox
Develop a program to create a option menu using checkboxes and display the toast selected checkboxes with Android Studio
## AIM:
To Develop a program for creating a option menu using checkboxes and display the toast selected checkboxes with Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Once the Selected check box displayed to the user processed in MainActivity.java

Step 7: Save and run the application.


## Program:
 ```
/*
Program to create an Option Menu
Developed by: Shaik Sameer Basha
RegisterNumber:  212222240093
*/
```

## MainActivity.java:
```
package com.example.checkbox;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.CheckBox;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
    private CheckBox chkAnd,chkjava,chkphp,chkcpp,chkC;
    Button btnDis;
    String selected;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        chkAnd=findViewById(R.id.chkAndroid);
        chkjava=findViewById(R.id.chkJava);
        chkphp=findViewById(R.id.chkPhp);
        chkcpp=findViewById(R.id.chkcpp);
        chkC=findViewById(R.id.chkC);
        btnDis=findViewById(R.id.btnDis);
        btnDis.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                selected = "you selected: \t";
                if(chkAnd.isChecked())
                {
                    selected += "Android\t";
                }
                if (chkjava.isChecked())
                {
                    selected += "Java\t";
                }
                if(chkcpp.isChecked())
                {
                    selected += "CPP\t";
                }if (chkphp.isChecked())
                {
                    selected += "PHP\t";
                }
                if (chkC.isChecked())
                {
                    selected += "C\t";
                }
                Toast.makeText(MainActivity.this,selected,Toast.LENGTH_SHORT).show();

            }
        });
    }


}
```
## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:orientation="vertical"
    android:padding="20dp">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Select Your favorite Programming Language"
        android:textStyle="bold"
        style="@style/TextAppearance.AppCompat.Large"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:gravity="center"
        android:layout_marginBottom="10dp"/>
    <CheckBox
        android:id="@+id/chkAndroid"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Android"
        style="@style/TextAppearance.AppCompat.Large"/>
    <CheckBox
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Java"
        style="@style/TextAppearance.AppCompat.Large"
        android:id="@+id/chkJava"/>
    <CheckBox
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="PHP"
        style="@style/TextAppearance.AppCompat.Large"
        android:id="@+id/chkPhp"/>
    <CheckBox
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="CPP"
        style="@style/TextAppearance.AppCompat.Large"
        android:id="@+id/chkcpp"/>
    <CheckBox
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="C"
        style="@style/TextAppearance.AppCompat.Large"
        android:id="@+id/chkC"/>
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="DISPLAY"
        android:id="@+id/btnDis"/>


</LinearLayout>
```


## AndroidMainfest.xml
```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.CheckBox"
        tools:targetApi="31">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

## Output

![8 1](https://github.com/shaikSameerbasha5404/Ex_8_CheckBox/assets/118707756/197dc4ba-1519-4b38-86dd-88572a8da883)


## Result:
Thus a Simple Android Application to create an check box and display the selected check box using Android Studio was developed and executed successfully.
