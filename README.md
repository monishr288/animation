# Ex.No: 11 Develop a application to add animations to ImageView,Move,blink,fade,clockwise,zoom,slide operations are perform in android studio.


## AIM:

To develop a application to add animation to imageview,move,blink,fade,clockwise,zoom,slide operation using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:
Step 1: Open Android Studio and then click on File → New → New Project.

Step 2: Then type the Application name as “Animation” and click Next.

Step 3: Then select the Minimum SDK as required and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design the layout in activity_main.xml with an ImageView and buttons for Move, Blink, Fade, Clockwise, Zoom, and Slide animations.

Step 6: Create separate animation XML files inside the res/anim/ folder for each animation and implement the logic in MainActivity.java to load and start each animation using AnimationUtils.

Step 7: Save and run the application to see different animations applied to the ImageView.


## PROGRAM:
```
/*
Program to display animation operation”.
Developed by: MONISH R
Registeration Number : 212223220061
*/
```
### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:gravity="center"
        android:padding="20dp">

        <ImageView
            android:id="@+id/imageView"
            android:layout_width="200dp"
            android:layout_height="200dp"
            android:src="@drawable/img"/>

        <Button
            android:id="@+id/btnMove"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Move"/>

        <Button
            android:id="@+id/btnBlink"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Blink"/>

        <Button
            android:id="@+id/btnFade"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Fade"/>

        <Button
            android:id="@+id/btnRotate"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Clockwise Rotate"/>

        <Button
            android:id="@+id/btnZoom"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Zoom"/>

        <Button
            android:id="@+id/btnSlide"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Slide"/>

    </LinearLayout>

</ScrollView>
```
## MainActivity.java
```
package com.example.imageanimationapp;


import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.animation.Animation;
import android.view.animation.AnimationUtils;
import android.widget.Button;
import android.widget.ImageView;

public class MainActivity extends AppCompatActivity {

    ImageView imageView;
    Button btnMove, btnBlink, btnFade, btnRotate, btnZoom, btnSlide;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        imageView = findViewById(R.id.imageView);

        btnMove = findViewById(R.id.btnMove);
        btnBlink = findViewById(R.id.btnBlink);
        btnFade = findViewById(R.id.btnFade);
        btnRotate = findViewById(R.id.btnRotate);
        btnZoom = findViewById(R.id.btnZoom);
        btnSlide = findViewById(R.id.btnSlide);

        btnMove.setOnClickListener(v -> {
            Animation anim = AnimationUtils.loadAnimation(this, R.anim.move);
            imageView.startAnimation(anim);
        });

        btnBlink.setOnClickListener(v -> {
            Animation anim = AnimationUtils.loadAnimation(this, R.anim.blink);
            imageView.startAnimation(anim);
        });

        btnFade.setOnClickListener(v -> {
            Animation anim = AnimationUtils.loadAnimation(this, R.anim.fade);
            imageView.startAnimation(anim);
        });

        btnRotate.setOnClickListener(v -> {
            Animation anim = AnimationUtils.loadAnimation(this, R.anim.rotate);
            imageView.startAnimation(anim);
        });

        btnZoom.setOnClickListener(v -> {
            Animation anim = AnimationUtils.loadAnimation(this, R.anim.zoom);
            imageView.startAnimation(anim);
        });

        btnSlide.setOnClickListener(v -> {
            Animation anim = AnimationUtils.loadAnimation(this, R.anim.slide);
            imageView.startAnimation(anim);
        });
    }
}
```

## OUTPUT
<img width="1763" height="894" alt="image" src="https://github.com/user-attachments/assets/7f335365-db50-4390-b9dd-7174d662d573" />
<img width="1767" height="915" alt="image" src="https://github.com/user-attachments/assets/d7297a80-29cb-4490-b1d9-1a809db93359" />





## RESULT
Thus an application to add animation to imageview,move,blink,fade,clockwise,zoom,slide operation using Android Studio is developed and executed successfully.
