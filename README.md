# Template to use OpenCV in QT

This single template allows to use [OpenCV] into a [QT] applicatio (`QMainWindow` based). Some  aspects to be considered:

* Initially, the project was created using QT Creator. However, I am not fan of that IDE/environment (*actually I hate it*). That is the reason that project contains a `.pro` file
* Next, the **QT Designer** was used it just to place a single `Label` widget
* Project is generated to work using **Visual Studio**. Then a [CMake] file is created manually (don't worry, it works)
* Files `mainview.*` are related to the graphical interface

File `mainview.cpp` contains the code to display an image, loading a simple image

>You need an image called `small.png` in the same location of the source/headers files (aka, the root). Actually, you must to change that!

### Setup

`OpenCVinQT` requires [CMake] to create the environment (I used the version 3.10).
Also, I used Visual Studio 2017 as IDE, and QT version 5.10, and VTK version 8.0.1 (December, 2017). 

### Note

Using a label to render/display an OpenCV image, is not a good approach (actually is a very bad approach! due that is slow and not resizable).

[Walter Lucetti](https://github.com/Myzhar "Myzhar") offers a better approach using [OpenGL to render the image](https://github.com/Myzhar/QtOpenCVViewerGl "QTOpenCVViewerGL") getting a faster, adjustable and coherent way to do that.

Of course, that is not the only approach available. Google has [a simple multithreaded OpenCV example application using the Qt framework](https://code.google.com/archive/p/qt-opencv-multithreaded/) which looks very nice to test and to incorporate into projects.

###### If you want to contribute? Great!
[OpenCV]: <https://opencv.org/>
[QT]: <https://www.qt.io/>
[CMake]: <https://cmake.org/>