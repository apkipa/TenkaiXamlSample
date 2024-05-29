# TenkaiXamlSample

A simple project to demonstrate how to create XAML Islands applications with `Tenkai.UI.Xaml.Window`.

#### Features

* UWP-like development experience with traditional Win32 API support.
* Flexible & friendly (i.e. UWP-like) title bar customization.
* Supports XAML hot reloading.
* Single-exe output (a single UWP exe, unlike the [official guide](https://learn.microsoft.com/en-us/windows/apps/desktop/modernize/host-custom-control-with-xaml-islands-cpp) which requires one UWP dll + one Win32 exe).
* Smooth window resizing (works partially; might not work for too old or too new OSs).

#### Unimplemented

* Changing window view mode (Fullscreen, CompactOverlay).
* Adapt to auto-hide taskbars.
* Support for light/dark theme switching is limited.
* Cross-platform support for PC UWP and XAML Islands.
* Skipping splash screen (currently it is not possible to disable splash animations due to technical limitations).
* Controls like `Tenkai.UI.Xaml.Controls.AdaptiveGridView`.
* Use Win11 frame style for Win11.

## Building

Restore NuGet packages first by adding the private feed to your IDE (note that the package is experimental and APIs are subject to heavy changes!):

```
https://baget.apkipa.eu.org/v3/index.json
```

Due to limitations of Visual Studio, you must manually set the meta project `TenkaiXamlSample.Win32` as startup project and untick *Deploy* checkboxes in *Configuration Manager* before building, otherwise Visual Studio will deploy the exe as a pure UWP application, causing the execution to fail.