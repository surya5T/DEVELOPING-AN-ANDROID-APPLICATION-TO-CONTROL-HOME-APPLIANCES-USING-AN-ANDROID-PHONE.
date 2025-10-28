# DEVELOPING-AN-ANDROID-APPLICATION-TO-CONTROL-HOME-APPLIANCES-USING-AN-ANDROID-PHONE.

## AIM:
To develop an android application to control home appliances

## APPARATUS REQUIRED:

ØComputer
ØAndroid studio software


## THEORY:
The Appliance Control App provides a user interface to control appliances such as a fan, light, and air conditioner. The app consists of buttons to turn each appliance on or off, and the status of each appliance is displayed in real-time using TextViews. This experiment teaches the basics of creating a control panel-style user interface in Android, where multiple appliances can be managed independently. It involves handling button clicks to change the state of UI elements dynamically and reflects the principles of event-driven programming in Android. The app also demonstrates how to update the user interface based on user interactions with different components, enhancing user engagement.

## PROCEDURE:
1. Open Android Studio and then click on File -> New -> New project. 35. Then type the application name as “ex.no.4″ and click Next.
2. Then select the Minimum SDK as shown below and click next. 37. Then select the Empty Activity and click next.
3. Finally click Finish.
4. Click on app -> java -> com.example -> MainActivity.java
5. Now click on Text and type the program, so now the programming part of the main activity is completed.
6. Click on app -> res -> layout -> activity_main.xml.
7. Now click on Text and type the program, so now the designing part of Activity main is also completed.
8. Select the suitable available device to display the output. 44. Now run the application to see the output. 

## PROGRAM:
## MainActivity.java

 
```
package com.example.appliancecontrol;

 

import android.os.Bundle; import android.view.View; import android.widget.*;

import androidx.appcompat.app.AppCompatActivity;

 

public class MainActivity extends AppCompatActivity {

 

TextView fanStatus, lightStatus, acStatus;

Button fanOn, fanOff, lightOn, lightOff, acOn, acOff;

 

@Override

protected void onCreate(Bundle savedInstanceState) { super.onCreate(savedInstanceState); setContentView(R.layout.activity_main);

 

fanStatus = findViewById(R.id.fanStatus); lightStatus = findViewById(R.id.lightStatus); acStatus = findViewById(R.id.acStatus);

 

fanOn = findViewById(R.id.fanOn); fanOff = findViewById(R.id.fanOff); lightOn = findViewById(R.id.lightOn); lightOff = findViewById(R.id.lightOff); acOn = findViewById(R.id.acOn); acOff = findViewById(R.id.acOff);

 

fanOn.setOnClickListener(v -> fanStatus.setText("Fan: ON")); fanOff.setOnClickListener(v -> fanStatus.setText("Fan: OFF"));

 

lightOn.setOnClickListener(v -> lightStatus.setText("Light: ON")); lightOff.setOnClickListener(v -> lightStatus.setText("Light: OFF"));

 

acOn.setOnClickListener(v -> acStatus.setText("AC: ON")); acOff.setOnClickListener(v -> acStatus.setText("AC: OFF"));

} }

 ```

## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>

<ScrollView xmlns:android="http://schemas.android.com/apk/res/android" android:layout_width="match_parent" android:layout_height="match_parent">

<LinearLayout android:layout_width="match_parent" android:layout_height="wrap_content" android:orientation="vertical" android:padding="20dp">

<TextView android:id="@+id/titleText"

android:layout_width="match_parent" android:layout_height="wrap_content" android:text="Appliance Control Panel" android:textSize="24sp" android:textStyle="bold" android:gravity="center" android:paddingBottom="20dp" />

<!-- Fan Control -->

<TextView android:id="@+id/fanStatus" android:layout_width="match_parent" android:layout_height="wrap_content" android:text="Fan: OFF" android:textSize="18sp" android:padding="8dp"/>

<LinearLayout android:layout_width="match_parent" android:layout_height="wrap_content" android:orientation="horizontal"> <Button

android:id="@+id/fanOn" android:layout_width="0dp" android:layout_weight="1" android:layout_height="wrap_content" android:text="Fan ON" />

<Button android:id="@+id/fanOff" android:layout_width="0dp" android:layout_weight="1"

android:layout_height="wrap_content" android:text="Fan OFF" />

</LinearLayout>

<!-- Light Control -->

<TextView android:id="@+id/lightStatus" android:layout_width="match_parent"

 

android:layout_height="wrap_content" android:text="Light: OFF" android:textSize="18sp" android:padding="8dp"/>

<LinearLayout android:layout_width="match_parent" android:layout_height="wrap_content" android:orientation="horizontal"> <Button

android:id="@+id/lightOn" android:layout_width="0dp" android:layout_weight="1" android:layout_height="wrap_content" android:text="Light ON" />

<Button android:id="@+id/lightOff" android:layout_width="0dp" android:layout_weight="1"

android:layout_height="wrap_content" android:text="Light OFF" />

</LinearLayout> <!-- AC Control -->

<TextView android:id="@+id/acStatus" android:layout_width="match_parent" android:layout_height="wrap_content" android:text="AC: OFF" android:textSize="18sp" android:padding="8dp"/>

<LinearLayout android:layout_width="match_parent" android:layout_height="wrap_content" android:orientation="horizontal"> <Button

android:id="@+id/acOn" android:layout_width="0dp" android:layout_weight="1" android:layout_height="wrap_content" android:text="AC ON" />

<Button android:id="@+id/acOff" android:layout_width="0dp" android:layout_weight="1"

android:layout_height="wrap_content" android:text="AC OFF" />

</LinearLayout> </LinearLayout>

</ScrollView>
```

## OUTPUT: 
<img width="1920" height="1080" alt="Screenshot 2025-10-14 155438" src="https://github.com/user-attachments/assets/47e2519b-3c22-409c-8ef5-840a9c262a23" />


## RESULT:
Thus, the Android app for controlling home appliances is developed and the output is verified.
