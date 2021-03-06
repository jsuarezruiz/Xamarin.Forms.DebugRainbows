<img src="https://github.com/sthewissen/Xamarin.Forms.DebugRainbows/blob/master/images/icon.png" width="150px" />

# Xamarin.Forms.DebugRainbows
The package you didn't even know you needed!

[![Build status](https://sthewissen.visualstudio.com/DebugRainbows/_apis/build/status/DebugRainbows-Deployment-CI)]() ![](https://img.shields.io/nuget/vpre/Xamarin.Forms.DebugRainbows.svg)

## Why DebugRainbows?

Have you ever had a piece of XAML code that didn't produce the layout you expected? Did you change background colors on certain elements to get an idea of where they are positioned? Admit it, you have and pretty much all of us have at some point. Either way, this is the package for you! It adds a very colorful debug mode to each of your `ContentPage`s that lets you immediately see where all of your elements are located!

<img src="https://raw.githubusercontent.com/sthewissen/Xamarin.Forms.DebugRainbows/master/images/sample.png" />

## How to use it?

The project is up on NuGet at the following URL:

https://www.nuget.org/packages/Xamarin.Forms.DebugRainbows

Install this package into your shared project. There is no need to install it in your platform specific projects. After that you're good to go! Simply add the namespace declaration and the new `IsDebug` attached property and set it to `true`!

```
<ContentPage rainbows:DebugRainbow.IsDebug="true" 
   xmlns="http://xamarin.com/schemas/2014/forms" 
   xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml" 
   xmlns:rainbows="clr-namespace:Xamarin.Forms.DebugRainbows;assembly=Xamarin.Forms.DebugRainbows" 
   x:Class="SampleApp.MainPage">
             
  ...
             
</ContentPage>
```

Want to apply it to each page in your app? You can do that by adding this `Style` to a `ResourceDictionary` in your `App.xaml` file.

```
<Style ApplyToDerivedTypes="True" TargetType="ContentPage">
   <Setter Property="debug:DebugRainbow.IsDebug" Value="false" />
</Style>
```
