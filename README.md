ChipLayout
==========

ChipLayout is an opensource Android library. ChipLayout is an layout which create chips from the text you type and also allow you to show drop down(like MultiautocompleteTextView)

Example
-------

### Screenshots
![Screenshot 1](https://github.com/OfficialAmal/ChipLayout/tree/master/img/img1.png)

![Screenshot 2](https://github.com/OfficialAmal/ChipLayout/tree/master/img/img2.png)

Source code with examples is included in repository.

Usage
-----
```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:custom="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#FFF"
    android:padding="10dp"
    android:orientation="vertical">
    <com.libaml.android.view.chip.ChipLayout
        android:id="@+id/chipText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        custom:textSize_="10dp"
        custom:chipPadding_="4dp"
        custom:chipTextPadding_="2dp"
        custom:textColor_="@android:color/black"
        custom:deleteIcon_="@android:drawable/presence_offline"
        custom:chipDrawable_="@drawable/round_corner_drawable"
        custom:chipLayoutDrawable_="@drawable/edittext_theme_landing_page"
        custom:labelPosition_="left">
    </com.libaml.android.view.chip.ChipLayout>
</LinearLayout>

```
======
Find the View in your Activity or Fragment class.

```java
  ChipLayout chip = (ChipLayout) findViewById(R.id.chipText);
        
        String[] countries = {"india","australia","austria","indonesia","canada"};
        ArrayAdapter<String> adapter = new ArrayAdapter<String>(this,android.R.layout.simple_list_item_1,countries);
        chip.setAdapter(adapter);

        chip.setOnClickListener(ClickListener);
        chip.setOnItemClickListener(ItemClickListener);
        chip.addLayoutTextChangedListener(TextChangedListener);
        chip.setOnFocusChangeListener(FocusChangeListener);
```

XML attributes 

 	        textSize_  		    	format=  dimension  
            chipPadding_   		    format=  dimension  
            chipPaddingLeft_   		format=  dimension  
            chipPaddingRight_  		format=  dimension  
            chipPaddingTop_   		format=  dimension  
            chipPaddingBottom_  	format=  dimension  
            chipTextPadding_   		format=  dimension  
            chipTextPaddingLeft_   	format=  dimension  
            chipTextPaddingRight_  	format=  dimension  
            chipTextPaddingTop_   	format=  dimension  
            chipTextPaddingBottom_  format=  dimension  
            textColor_      		format=  color   
            chipColor_   		    format=  color   
            showText_   	    	format=  boolean   
            showDeleteButton_   	format=  boolean   
            deleteIcon_   	    	format=  reference   
            chipDrawable_   		format=  reference   
            chipLayoutDrawable_   	format=  reference   
            labelPosition_   		format=  (left/right) 
          
Public Methods

            public void setOnClickListener(OnClickListener l)
            public void setOnItemClickListener(AdapterView.OnItemClickListener l) 
            public void removeChipAt(int pos)
            public void setAdapter(ArrayAdapter adapter)
            public void setText(List<String> vals)
            public void addLayoutTextChangedListener(TextWatcher textWatcher)
            public void removeLayoutTextChangedListener(TextWatcher textWatcher)
            public void setTextColor(int textColor)
            public void setChipColor(int bgColor)

            public AdapterView.OnItemClickListener getOnItemClickListener()
            public int getTextColor()
            public int getChipColor()
            public List<String> getText()
            public ArrayAdapter getAdapter()
            
Dependencies
------------
### Gradle
```
compile 'com.libaml.android.view.chip:AndroidChipLayout:1.0.1'
```
