libgstreamersharpglue
=====================

To use gstreamer on Windows from .NET 3 dlls are required:
+ glib-sharp
+ gstreamer-sharp
+ libgstreamersharpglue-1.0.0

The first two dlls are managed dll which are the same on Linux and Windows. They can be compiled from the [gtk-sharp](https://github.com/mono/gtk-sharp) and [gstreamer-sharp](http://cgit.freedesktop.org/gstreamer/gstreamer-sharp/) code on a Linux system.
The latter is a native library which helps glue the managed .NET interfaces with the native gstreamer interfaces. When compiling the gstreamer-sharp project, this glue is put in a Linux shared object library. This library isn't usable directly on Windows. [These instructions on stackoverflow](http://stackoverflow.com/questions/21577733/how-to-build-gstreamer-sharp-with-monodevelop-xamarin/21607884#21607884) explain how the equivalent Windows dll can be created. The Visual Studio project in this repository is the result of applying the instructions and allows to create the libgstreamersharpglue dll for Windows.

The releases of this github project contain all three dlls.
