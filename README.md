# BiColored Progress
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/vlad1m1r990/Lemniscate/blob/master/LICENSE)
[![](https://jitpack.io/v/arbelkilani/BiColored-Progress.svg)](https://jitpack.io/#arbelkilani/BiColored-Progress)
[![API](https://img.shields.io/badge/API-19%2B-green.svg?style=flat)]()

Awsome animated a bi-colored circular progress.

![biColored](https://i.makeagif.com/media/3-29-2018/DKzRJE.gif)

## Setup

Add to your module's build.gradle:

```xml
allprojects {
        repositories {
            ...
            maven { url 'https://jitpack.io' }
        }
    }
```
and to your app build.gradle:

```xml
dependencies {
  implementaion 'com.github.arbelkilani:BiColored-Progress:v1.2'
}
```

## Usage

```xml
<com.arbelkilani.bicoloredprogress.BiColoredProgress
        android:id="@+id/twice_colored_progress"
        android:layout_width="150dp"
        android:layout_height="150dp"
        app:duration="4000" 
        app:inner_alpha_factor="0.3" 
        app:label="Total gain" 
        app:left_sided_color="@color/colorAccent"
        app:right_sided_color="@color/colorPrimary"
        app:stroke_width="4dp" />
```

###### Params available in all views:

* **duration** (int) - duration of one animation 
* **label** (String) - optional 
* **left_sided_color** (color) - left sided color
* **right_sided_color** (color) - right sided color
* **stroke_width** (float) - outsider circle stroke width
* **inner_alpha_factor** (float) - alpha value from outsider to inner color

###### Animation interpolator:
```java

BiColoredProgress biColoredProgress = findViewById(R.id.twice_colored_progress);

biColoredProgress.setProgress(87f);
biColoredProgress.setAnimated(true, 4000, new BounceInterpolator());
```

###### setAnimated attributes :
```java

/**
     * 
     * @param canAnimate : boolean, true if want to have animated progress
     * @param animationDuration : int, animation duration
     * @param interpolator : Interpolator, either basic or custom animation interpolator
 */
    public void setAnimated(boolean canAnimate, int animationDuration, Interpolator interpolator) {}
```


## License

    Copyright 2018 Belkilani Ahmed Radhouane

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
