# Toastly

fork from [Toasty: The usual Toast, but with steroids](https://github.com/GrenderG/Toasty)

[![API](https://img.shields.io/badge/API-14%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=14) [![](https://jitpack.io/v/GrenderG/Toasty.svg)](https://jitpack.io/#GrenderG/Toasty) [![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-Toasty-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/5102) [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.me/grenderg)

<div align="center">
	<img src="https://raw.githubusercontent.com/GrenderG/Toasty/master/art/web_hi_res_512.png" width="128">
</div>

The usual Toast, but with steroids.

## Configuration

This step is optional, but if you want you can configure some Toasty parameters. Place this anywhere in your app:

```java
Toasty.Config.getInstance()
    .tintIcon(boolean tintIcon) // optional (apply textColor also to the icon)
    .setToastTypeface(@NonNull Typeface typeface) // optional
    .setTextSize(int sizeInSp) // optional
    .allowQueue(boolean allowQueue) // optional (prevents several Toastys from queuing)
    .apply(); // required
```

You can reset the configuration by using `reset()` method:

```java
Toasty.Config.reset();
```

## Usage

Each method always returns a `Toast` object, so you can customize the Toast much more. **DON'T FORGET THE `show()` METHOD!**

To display an error Toast:

``` java
Toasty.error(yourContext, "This is an error toast.", Toast.LENGTH_SHORT, true).show();
```
To display a success Toast:

``` java
Toasty.success(yourContext, "Success!", Toast.LENGTH_SHORT, true).show();
```
To display an info Toast:

``` java
Toasty.info(yourContext, "Here is some info for you.", Toast.LENGTH_SHORT, true).show();
```
To display a warning Toast:

``` java
Toasty.warning(yourContext, "Beware of the dog.", Toast.LENGTH_SHORT, true).show();
```
To display the usual Toast:

``` java
Toasty.normal(yourContext, "Normal toast w/o icon").show();
```
To display the usual Toast with icon:

``` java
Toasty.normal(yourContext, "Normal toast w/ icon", yourIconDrawable).show();
```

You can also create your custom Toasts with the `custom()` method:
``` java
Toasty.custom(yourContext, "I'm a custom Toast", yourIconDrawable, tintColor, duration, withIcon, 
shouldTint).show();
```
### Extra
[You can pass formatted text to Toasty!](https://github.com/GrenderG/Toasty/blob/master/app/src/main/java/es/dmoral/toastysample/MainActivity.java#L98-L107)

**There are variants of each method, feel free to explore this library.**

## Screenshots

**Please click the image below to enlarge.**

<img src="https://raw.githubusercontent.com/GrenderG/Toasty/master/art/collage.png">

## Third Party Bindings

### React Native
You may now use this library with [React Native](https://github.com/facebook/react-native) via this [module](https://github.com/prscX/react-native-toasty).

