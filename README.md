# Android_Note
My_App
## Button
''''<Button
    android:id="@+id/button"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="Button"
    android:textAllCaps="false"/>''''//是否显示大写
- 两种方式：
- 一、
''''Public class MainActivity extends AppCompatActivity{
      @Override
      protected void onCreate(Bundle savedInstanceState){
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button button = (Button) findViewById(R.id.button);
        button.setOnClickListener(new View.OnClickListener(){
          @Override
          public void onClick(View v){
            //
          }
        });
      }
    }''''
- 二、
''''Public class MainActivity extends AppCompatActivity{
      @Override
      protected void onCreate(Bundle savedInstanceState){
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button button = (Button) findViewById(R.id.button);
        button.setOnClickListener(this);
      }
      @Override
      public void onClick(View v){
        switch(v.getId()){
        case R.id.button:
          //
          break;
        default:
          break;
        }
      }
    }''''
