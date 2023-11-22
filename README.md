# intent_mobile


 <h4><br>Nama Abdul Aziz</br>
 <br>Kelas : Ti 22.A.1</br>
 <br>NIm : 312210022</br></h4>


# kodingan activity main
           
                      <?xml version="1.0" encoding="utf-8"?>
           <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
               xmlns:tools="http://schemas.android.com/tools"
               android:layout_width="match_parent"
               android:layout_height="match_parent"
               tools:context=".MainActivity">
           
               <ImageView
                   android:id="@+id/background"
                   android:layout_width="match_parent"
                   android:layout_height="match_parent"
                   android:adjustViewBounds="true"
                   android:scaleType="centerCrop"
                   android:src="@drawable/background" />
           
               <Button
                   android:id="@+id/btnHelloWorld"
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:onClick="btnHelloWorld"
                   android:layout_centerHorizontal="true"
                   android:layout_marginTop="200dp"
                   android:text="@string/project_hello"
                   tools:ignore="UsingOnClickInXml" />
           
               <Button
                   android:id="@+id/btnProjectCount"
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:onClick="btnCount"
                   android:layout_below="@+id/btnHelloWorld"
                   android:layout_centerHorizontal="true"
                   android:layout_marginTop="20dp"
                   android:text="@string/project_count"
                   tools:ignore="UsingOnClickInXml" />
           
               <Button
                   android:id="@+id/btnProjectSianida"
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:onClick="btnSianida"
                   android:layout_below="@+id/btnProjectCount"
                   android:layout_centerHorizontal="true"
                   android:layout_marginTop="20dp"
                   android:text="@string/article_subtitle"
                   tools:ignore="UsingOnClickInXml" />
           
               <Button
                   android:id="@+id/btnTwoActivity"
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:onClick="btnTwoActivity"
                   android:layout_below="@+id/btnProjectSianida"
                   android:layout_centerHorizontal="true"
                   android:layout_marginTop="20dp"
                   android:text="@string/project_twoactivity"
                   tools:ignore="UsingOnClickInXml"
                   />
               <Button
                   android:id="@+id/btnSetAlarm"
                   android:layout_width="wrap_content"
                   android:layout_height="wrap_content"
                   android:onClick="btnSetAlarm"
                   android:layout_below="@+id/btnTwoActivity"
                   android:layout_centerHorizontal="true"
                   android:layout_marginTop="20dp"
                   android:text="@string/project_set_alarm"
                   tools:ignore="UsingOnClickInXml" />
           
           </RelativeLayout>


# main activity

         
            package com.example.tugas9;
         
         import androidx.appcompat.app.AppCompatActivity;
         
         import android.os.Bundle;
         
         import androidx.appcompat.app.AppCompatActivity;
         
         import android.content.Intent;
         import android.os.Bundle;
         import android.view.View;
         
         public class MainActivity extends AppCompatActivity {
         
             @Override
             protected void onCreate(Bundle savedInstanceState) {
                 super.onCreate(savedInstanceState);
                 setContentView(R.layout.activity_main);
         
                 findViewById(R.id.btnSetAlarm).setOnClickListener(new View.OnClickListener() {
                     @Override
                     public void onClick(View v) {
                         // Panggil metode untuk mengatur alarm
                         setAlarm();
                     }
                 });
             }
             private void setAlarm() {
                 Intent alarm = new Intent(android.provider.AlarmClock.ACTION_SET_ALARM);
                 startActivity(alarm);
             }
         
             public void btnHelloWorld(View view) {
                 Intent helloworld = new Intent(MainActivity.this, hello.class);
                 startActivity(helloworld);
             }
         
             public void btnCount(View view) {
                 Intent count = new Intent(MainActivity.this, count.class);
                 startActivity(count);
             }
         
             public void btnSianida(View view) {
                 Intent sianida = new Intent(MainActivity.this, SianidaActivity.class);
                 startActivity(sianida);
             }
         
             public void btnTwoActivity(View view) {
                 Intent twoact = new Intent(MainActivity.this, twoactivity.class);
                 startActivity(twoact);
             }
         }


# hasil run


https://github.com/lampubohlam/intent_mobile/assets/116137169/21899905-d8fe-494b-b90d-90d8ec6fdcc9


                   
