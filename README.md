# BubbleView
Bubble view for Android

 [ ![Download](https://api.bintray.com/packages/jaredlam/maven/BubbleView/images/download.svg) ](https://bintray.com/jaredlam/maven/BubbleView/_latestVersion)

![alt tag](https://raw.githubusercontent.com/jaredlam/BubbleView/master/Bubble.gif)

- [Introduction](#introduction)
- [Download](#download)
- [Usage](#usage)
- [License](#license)

# Introduction

- Bubble layout will generate Bubble view at random location on screen.

- Bubble view is extend from TextView.

- Bubble views will bounce with each other.

- Bubble layout will try to contains all child inside its bounds.

- Support gestures.

# Download
```groovy
dependencies {
    compile 'com.jaredlam.bubbleview:library:0.1.1'
}
```

# Usage

```xml
    <com.jaredlam.bubbleview.BubbleLayout
        android:id="@+id/bubble_layout"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:bubbleview_maxSpeed="3dp"
        app:bubbleview_minSpeed="1dp"
        app:bubbleview_padding="10dp" />
```

```java
BubbleLayout layout = (BubbleLayout) findViewById(R.id.bubble_layout);

for (String label : labels) {
    BubbleView bubbleView = new BubbleView(this);
    bubbleView.setText(label);
    bubbleView.setGravity(Gravity.CENTER);
    bubbleView.setPadding(10, 10, 10, 10);
    bubbleView.setTextColor(Color.parseColor("#000000"));
    layout.addViewSortByWidth(bubbleView);
}
```

# License

Copyright (C) 2015 Jared Luo
jaredlam86@gmail.com

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.










