
This is a fork from https://github.com/daimajia/AndroidImageSlider
#
with these changes

** ✓  replace picasso with Glide  

** ⌛  kotlin demo 

** ⌛  fix issues

#
# Android Image Slider 
[![Release](https://jitpack.io/v/m0aaz/AndroidImageSlider.svg)]
(https://jitpack.io/#moaaz/AndroidImageSlider)

  
This is an amazing image slider for the Android platform. I decided to open source this because there is really not an attractive, convenient slider widget in Android.
 
You can easily load images from an internet URL, drawable, or file. And there are many kinds of amazing animations you can choose. :-D
 
## Demo
 
![](http://ww3.sinaimg.cn/mw690/610dc034jw1egzor66ojdg20950fknpe.gif)


## Usage

### Step 1

#### Gradle

```groovy
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}

dependencies {
    		dependencies {
        	        compile 'com.github.m0aaz:AndroidImageSlider:v1.2'
        	}
}
```


#### Maven

```xml

    <repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>



	<dependency>
    	 <groupId>com.github.m0aaz</groupId>
    	 <artifactId>AndroidImageSlider</artifactId>
    	 <version>v1.2</version>
    </dependency>

```

### Step 2

Add permissions (if necessary) to your `AndroidManifest.xml`

```xml
<!-- if you want to load images from the internet -->
<uses-permission android:name="android.permission.INTERNET" />

<!-- if you want to load images from a file OR from the internet -->
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />

```

**Note:** If you want to load images from the internet, you need both the `INTERNET` and `READ_EXTERNAL_STORAGE` permissions to allow files from the internet to be cached into local storage.

If you want to load images from drawable, then no additional permissions are necessary.

### Step 3

Add the Slider to your layout:

```xml
<com.daimajia.slider.library.SliderLayout
        android:id="@+id/slider"
        android:layout_width="match_parent"
        android:layout_height="200dp"
/>
```

There are some default indicators. If you want to use a provided indicator:

```xml
<com.daimajia.slider.library.Indicators.PagerIndicator
        android:id="@+id/custom_indicator"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:gravity="center"
        />
```
