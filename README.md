<h1 align="center">Beautiful Dialog</h1></br>
<p align="center"> 
🗨️ Beautiful Dialog is a Simple and Beautiful custom dialog.
</p>
</br>

<p align="center">
  <a href="https://opensource.org/licenses/Apache-2.0"><img alt="License" src="https://img.shields.io/badge/License-Apache%202.0-blue.svg"/></a>
  <a href="https://android-arsenal.com/api?level=21"><img alt="API" src="https://img.shields.io/badge/API-21%2B-brightgreen.svg?style=flat"/></a>
  <img alt="repo size" src="https://img.shields.io/github/repo-size/iamageo/beautiful-dialog"/>
  </br>
    <img alt="forks" src="https://img.shields.io/github/forks/iamageo/beautiful-dialog?style=social"/>
    <img alt="stars" src="https://img.shields.io/github/stars/iamageo/beautiful-dialog?style=social"/>

  
</p>

## Screenshots
<p align="center">
<img src="https://user-images.githubusercontent.com/26925002/162633413-8cc80819-5ff8-4258-b60e-5101d058c907.png" width="30%"/>
<img src="https://user-images.githubusercontent.com/26925002/162633421-653961c1-a77b-4009-945d-09618c6fd772.png" width="30%"/>
<img src="https://user-images.githubusercontent.com/26925002/162633431-38a1a45e-91b7-4a1a-b4ba-686fe440b8b5.png" width="30%"/>
</p>

## Including in your project
[![](https://jitpack.io/v/iamageo/beautiful-dialog.svg)](https://jitpack.io/#iamageo/beautiful-dialog)
### Gradle 
Add below codes to your **root** `build.gradle` file (not your module build.gradle file).
```gradle
allprojects {
  repositories {
    ...
    maven { url 'https://jitpack.io' }
  }
}
```
And add a dependency code to your **module**'s `build.gradle` file.
```gradle
dependencies {
        implementation 'com.github.iamageo:beautiful-dialog:Tag'
}
```

## Basic Usage
Add in you Activity file.

```kotlin
BeautifulDialog.build(this)
    .title("Title success", titleColor = R.color.black)
    .body("Description success",  color = R.color.black)
    .type(type= BeautifulDialog.TYPE.SUCCESS)
    .position(BeautifulDialog.POSITIONS.CENTER)
    .onPositive("Confirm") {
        Toast.makeText(this, "confirm", Toast.LENGTH_SHORT).show()
    }
    .onNegative("Cancel") {
        Toast.makeText(this, "cancel", Toast.LENGTH_SHORT).show()
    }

```

## Type ✔️ ℹ️ ❌
We can customize the type of Dialog.
```kotlin
TYPE.SUCCESS
TYPE.INFO
TYPE.ERROR
```
By Default Position is Bottom.

| SUCCESS | INFO | ERROR
| :---------------: | :---------------: | :---------------: | 
| <img src="https://user-images.githubusercontent.com/26925002/162633413-8cc80819-5ff8-4258-b60e-5101d058c907.png" align="center" width="50%"/> | <img src="https://user-images.githubusercontent.com/26925002/162633421-653961c1-a77b-4009-945d-09618c6fd772.png" align="center" width="50%"/> | <img src="https://user-images.githubusercontent.com/26925002/162633431-38a1a45e-91b7-4a1a-b4ba-686fe440b8b5.png" align="center" width="50%"/>


## Positioning 📱
We can customize the Position of Dialog.
```kotlin
POSITIONS.TOP
POSITIONS.CENTER
POSITIONS.BOTTOM
```
By Default Position is Bottom.

| TOP (with error) | CENTER | BOTTOM
| :---------------: | :---------------: | :---------------: | 
| <img src="https://user-images.githubusercontent.com/26925002/162633413-8cc80819-5ff8-4258-b60e-5101d058c907.png" align="center" width="50%"/> | <img src="https://user-images.githubusercontent.com/26925002/162633413-8cc80819-5ff8-4258-b60e-5101d058c907.png" align="center" width="50%"/> | <img src="https://user-images.githubusercontent.com/26925002/162633465-7dae6ed4-c638-432e-a823-7276e046546b.png" align="center" width="50%"/>


## Beautiful Dialog Attributes
Attributes | Type | Default | Description
--- | --- | --- | ---
title | String | none | Title of you dialog. 
description | String | none | Description of you dialog.
position | POSITIONS.BOTTOM, POSITIONS.CENTER, POSITIONS.TOP | POSITIONS.BOTTOM | Indicates the position of the dialog.
type | TYPE.SUCCESS, TYPE.INFO or TYPE.ERROR | none | Indicates the dialog type, each type contains an icon.
onPositive | onClick | none | Button positive click.
onNegative | onClick | none | Button negative click.

## License
```


    Copyright 2022 Geovani Amaral

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

```

