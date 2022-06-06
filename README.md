# Ex.No:7 Develop a simple calculator using android studio.
## AIM:
To develop a program to develop a simple calculator in Android Studio.

## EQUIPMENTS REQUIRED:
Android Studio(Min.required Artic Fox)

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as calculator and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the calculator operation in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```python
/*
Program to print the text “calculator operation”.
Developed by: Gowri M
Registeration Number : 212220230019
*/
```
## MainActivity.java
```python
package com.example.calculator;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;


public class MainActivity extends AppCompatActivity {

    double in1 = 0, i2 = 0;
    TextView edittext1;
    boolean Add, Sub, Multiply, Divide, Remainder, deci;
    Button button_0, button_1, button_2, button_3, button_4, button_5, button_6, button_7, button_8, button_9, button_Add, button_Sub,
            button_Mul, button_Div, button_Equ, button_Del, button_Dot, button_Remainder;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button_0 = (Button) findViewById(R.id.b0);
        button_1 = (Button) findViewById(R.id.b1);
        button_2 = (Button) findViewById(R.id.b2);
        button_3 = (Button) findViewById(R.id.b3);
        button_4 = (Button) findViewById(R.id.b4);
        button_5 = (Button) findViewById(R.id.b5);
        button_6 = (Button) findViewById(R.id.b6);
        button_7 = (Button) findViewById(R.id.b7);
        button_8 = (Button) findViewById(R.id.b8);
        button_9 = (Button) findViewById(R.id.b9);
        button_Dot = (Button) findViewById(R.id.bDot);
        button_Add = (Button) findViewById(R.id.badd);
        button_Sub = (Button) findViewById(R.id.bsub);
        button_Mul = (Button) findViewById(R.id.bmul);
        button_Div = (Button) findViewById(R.id.biv);
        button_Remainder = (Button) findViewById(R.id.BRemain);
        button_Del = (Button) findViewById(R.id.buttonDel);
        button_Equ = (Button) findViewById(R.id.buttoneql);

        edittext1 = (TextView) findViewById(R.id.display);

        button_1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edittext1.setText(edittext1.getText() + "1");
            }
        });

        button_2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edittext1.setText(edittext1.getText() + "2");
            }
        });

        button_3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edittext1.setText(edittext1.getText() + "3");
            }
        });

        button_4.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edittext1.setText(edittext1.getText() + "4");
            }
        });

        button_5.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edittext1.setText(edittext1.getText() + "5");
            }
        });

        button_6.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edittext1.setText(edittext1.getText() + "6");
            }
        });

        button_7.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edittext1.setText(edittext1.getText() + "7");
            }
        });

        button_8.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edittext1.setText(edittext1.getText() + "8");
            }
        });

        button_9.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edittext1.setText(edittext1.getText() + "9");
            }
        });

        button_0.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edittext1.setText(edittext1.getText() + "0");
            }
        });

        button_Add.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if (edittext1.getText().length() != 0) {
                    in1 = Float.parseFloat(edittext1.getText() + "");
                    Add = true;
                    deci = false;
                    edittext1.setText(null);
                }
            }
        });

        button_Sub.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if (edittext1.getText().length() != 0) {
                    in1 = Float.parseFloat(edittext1.getText() + "");
                    Sub = true;
                    deci = false;
                    edittext1.setText(null);
                }
            }
        });

        button_Mul.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if (edittext1.getText().length() != 0) {
                    in1 = Float.parseFloat(edittext1.getText() + "");
                    Multiply = true;
                    deci = false;
                    edittext1.setText(null);
                }
            }
        });

        button_Div.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if (edittext1.getText().length() != 0) {
                    in1 = Float.parseFloat(edittext1.getText() + "");
                    Divide = true;
                    deci = false;
                    edittext1.setText(null);
                }
            }
        });

        button_Remainder.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if (edittext1.getText().length() != 0) {
                    in1 = Float.parseFloat(edittext1.getText() + "");
                    Remainder = true;
                    deci = false;
                    edittext1.setText(null);
                }
            }
        });

        button_Equ.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if (Add || Sub || Multiply || Divide || Remainder) {
                    i2 = Float.parseFloat(edittext1.getText() + "");
                }

                if (Add) {

                    edittext1.setText(in1 + i2 + "");
                    Add = false;
                }

                if (Sub) {

                    edittext1.setText(in1 - i2 + "");
                    Sub = false;
                }

                if (Multiply) {
                    edittext1.setText(in1 * i2 + "");
                    Multiply = false;
                }

                if (Divide) {
                    edittext1.setText(in1 / i2 + "");
                    Divide = false;
                }
                if (Remainder) {
                    edittext1.setText(in1 % i2 + "");
                    Remainder = false;
                }
            }
        });

        button_Del.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                edittext1.setText("");
                in1 = 0.0;
                i2 = 0.0;
            }
        });

        button_Dot.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if (deci) {
                    //do nothing or you can show the error
                } else {
                    edittext1.setText(edittext1.getText() + ".");
                    deci = true;
                }

            }
        });
    }
}
```
## activity_mian.xml
```python
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"

    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#ecf0f1"
    android:orientation="vertical">


    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0.3"
        android:orientation="horizontal">

        <TextView
            android:id="@+id/display"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:background="#ecf0f1"
            android:textSize="30sp" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0.2"
        android:orientation="horizontal">

        <Button
            android:id="@+id/buttonDel"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:background="@color/black"
            android:text="Del"
            android:textColor="#C51135"
            android:textSize="30sp" />

        <Button
            android:id="@+id/buttoneql"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:text="Answer"
            android:background="@color/black"
            android:textColor="#43D623"
            android:textSize="30sp" />

    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0.2"
        android:orientation="horizontal">

        <Button
            android:id="@+id/b1"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:background="@color/teal_200"
            android:text="1"
            android:textColor="@color/black"
            android:textSize="20sp" />

        <Button
            android:id="@+id/b2"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:background="@color/teal_200"
            android:text="2"
            android:textColor="@color/black"
            android:textSize="20sp" />

        <Button
            android:id="@+id/b3"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:background="@color/teal_200"
            android:text="3"
            android:textColor="@color/black"
            android:textSize="20sp" />

        <Button
            android:id="@+id/biv"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:text="/"
            android:background="#EDAE51"
            android:textColor="@color/black"
            android:textSize="30sp" />

    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0.2"
        android:orientation="horizontal">

        <Button
            android:id="@+id/b4"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:background="@color/teal_200"
            android:text="4"
            android:textColor="@color/black"
            android:textSize="20sp" />

        <Button
            android:id="@+id/b5"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:background="@color/teal_200"
            android:text="5"
            android:textColor="@color/black"
            android:textSize="20sp" />

        <Button
            android:id="@+id/b6"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:background="@color/teal_200"
            android:text="6"
            android:textColor="@color/black"
            android:textSize="20sp" />

        <Button
            android:id="@+id/bsub"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:text="-"
            android:background="#EDAE51"
            android:textColor="@color/black"
            android:textSize="30sp" />

    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0.2"
        android:orientation="horizontal">

        <Button
            android:id="@+id/b7"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:background="@color/teal_200"
            android:text="7"
            android:textColor="@color/black"
            android:textSize="20sp" />

        <Button
            android:id="@+id/b8"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:background="@color/teal_200"
            android:text="8"
            android:textColor="@color/black"
            android:textSize="20sp" />

        <Button
            android:id="@+id/b9"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:background="@color/teal_200"
            android:text="9"
            android:textColor="@color/black"
            android:textSize="20sp" />

        <Button
            android:id="@+id/bmul"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:text="x"
            android:background="#EDAE51"
            android:textColor="@color/black"
            android:textSize="30sp" />

        <Button
            android:id="@+id/BRemain"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:text="%"
            android:background="#EDAE51"
            android:textColor="@color/black"
            android:textSize="30sp" />

    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0.2"
        android:orientation="horizontal">

        <Button
            android:id="@+id/bDot"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:text="."
            android:background="#EDAE51"
            android:textColor="@color/black"
            android:textSize="50sp" />

        <Button
            android:id="@+id/b0"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:text="0"
            android:background="@color/teal_200"
            android:textColor="@color/black"
            android:textSize="20sp" />

        <Button
            android:id="@+id/badd"
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:layout_margin="1dp"
            android:layout_weight="0.25"
            android:onClick="onClick"
            android:text="+"
            android:background="#EDAE51"
            android:textColor="@color/black"
            android:textSize="30sp" />

    </LinearLayout>


</LinearLayout>
```
## OUTPUT
![p1](https://user-images.githubusercontent.com/75235704/172091468-1f090fe8-5a05-4922-ac2b-95ec11e54640.PNG)

![p2](https://user-images.githubusercontent.com/75235704/172091474-3305a75f-a9c9-40be-9e82-5de457926e36.PNG)


## RESULT
Thus a Simple Android Application develop a program to create simple calculator in Android Studio is developed and executed successfully.
