# Android Application for Addition of Two Numbers

## NAME:Marxin Lijo M
## REG NO: 212223240085

## Aim

To create an Android application that accepts two numbers from the user and displays their sum.

## Description

This is a simple Android application developed using **Android Studio, Java, and XML**. The user enters two numbers and clicks the **ADD** button to calculate and display their sum.

## Technologies Used

- Android Studio
- Java
- XML

## Features

- Accepts two numbers
- Performs addition
- Displays the sum
- Simple and user-friendly interface

## activity_main.xml

```
<?xml version="1.0" encoding="utf-8"?>

<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter First Number"
        android:inputType="numberDecimal" />

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Second Number"
        android:inputType="numberDecimal" />

    <Button
        android:id="@+id/btnAdd"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="ADD" />

    <TextView
        android:id="@+id/txtResult"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="20dp"
        android:text="Result"
        android:textSize="22sp" />

</LinearLayout>
```

## MainActivity.java

```java
package com.example.additionapp;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button btnAdd;
    TextView txtResult;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        btnAdd = findViewById(R.id.btnAdd);
        txtResult = findViewById(R.id.txtResult);

        btnAdd.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {

                double number1 = Double.parseDouble(
                        num1.getText().toString());

                double number2 = Double.parseDouble(
                        num2.getText().toString());

                double sum = number1 + number2;

                txtResult.setText("Sum = " + sum);
            }
        });
    }
}
```

## Output

**Input:**
- First Number: 25
- Second Number: 17.5

**Output:**

<img width="1740" height="904" alt="image" src="https://github.com/user-attachments/assets/8b649cfa-c0a6-47b5-bf00-b5aa5f50282e" />


## Result

The Android application for addition of two numbers was successfully created and executed using Android Studio.
