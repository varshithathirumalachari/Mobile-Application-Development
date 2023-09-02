# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by:varshitha A T
Registeration Number :212221040176
*/
```
## Activity_xml File:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">

<EditText
    android:id="@+id/numberEditText1"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginTop="172dp"
    android:ems="10"
    android:inputType="textPersonName"
    android:text=""
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.497"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />

<Button
    android:id="@+id/factorialButton"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginTop="340dp"
    android:text="Button"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.498"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## Activity_xml 2 File:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".FactorialActivity">

<TextView
    android:id="@+id/factorialTextView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginTop="283dp"
    android:text="TextView"
    android:textSize="36dp"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java File:
```
package com.example.factorialexplicit;

import static com.example.factorialexplicit.R.id.factorialButton;
import static com.example.factorialexplicit.R.id.numberEditText1;

import androidx.appcompat.app.AppCompatActivity;

import android.annotation.SuppressLint;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {
private EditText numberEditText;
private Button factorialButton;

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);

    numberEditText = findViewById(R.id.numberEditText1);
    factorialButton = findViewById(R.id.factorialButton);

    factorialButton.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View v) {
            int number = Integer.parseInt(numberEditText.getText().toString());

            Intent intent = new Intent(MainActivity.this, FactorialActivity.class);
            intent.putExtra("number", number);
            startActivity(intent);
        }
    });
}
}
```

## OUTPUT
![l](https://user-images.githubusercontent.com/128135244/241409051-562f5eee-68f6-4af8-ac16-05562c175bc9.png)

![p](https://user-images.githubusercontent.com/128135244/241409065-78bb6cd7-6ef2-405d-9abd-307aea56081a.png)

![k](https://user-images.githubusercontent.com/128135244/241409077-ee826d51-7938-4296-bc43-2a1a010733ce.png)


## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


