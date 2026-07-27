# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## Algorithm

### Step 1:
Create a new Android Studio project with an Empty Views Activity.

### Step 2:
Design the user interface in the `activity_main.xml` file by adding an `EditText` for entering a URL and a `Button` labeled **Search** or **Implicit Intent**.

### Step 3:
In `MainActivity.java`, initialize the `EditText` using the `findViewById()` method.

### Step 4:
Retrieve the URL entered by the user from the `EditText` when the button is clicked.

### Step 5:
Create an Implicit Intent using `Intent.ACTION_VIEW` and pass the URL as a `Uri`.

### Step 6:
Launch the intent using the `startActivity()` method to open the webpage in the device's default web browser.

### Step 7:
Run the application, enter a valid URL (e.g., `https://www.gmail.com`), and verify that the webpage opens successfully.


## PROGRAM:
```

Program to print the text “Implicitintent”.
Developed by: Niranjani.c
Registeration Number : 212223220069

package com.example.gmail;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;


public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        EditText editText;
        Button button;
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button = findViewById(R.id.btn);
        editText = (EditText) findViewById(R.id.editText);
        button.setOnClickListener(new View.OnClickListener()
        {
            @Override
            public void onClick(View view)
            {
               String url = editText.getText().toString();
               Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
               startActivity(intent);
            }
        });

    }
}

```

## OUTPUT

<img width="1917" height="1011" alt="Screenshot 2026-07-27 141642" src="https://github.com/user-attachments/assets/775be71b-1d33-4576-a2a1-54a6f7eccf5b" />
<img width="1917" height="1020" alt="Screenshot 2026-07-27 141537" src="https://github.com/user-attachments/assets/f61556a8-32e5-488b-93fb-06d9ff8ccea0" />



## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


