TempestSDR
=============

This project is in its infancy and is not operational! Please come back in Q2 of 2014 for more information about what it is and how to use :)

Folder Structure
------------

The different folders contain the different subprojects. The TempestSDR folder contains the main C library. The project aims to be crossplatform with plugin support for SDR frontends in different folders.

Requirements for Building
------------

The project is built with Eclipse with the CDT plugin (but this is not required). Currently it supports Windows and Linux. Some frontend plugins might not be crossplatform. You also need a Java Development Kit (JDK) installed.

### Windows

You need to have MinGW installed and gcc and make commands need to be in your path. Also javac and javah also need to be in your path.

### Linux

To be announced soon.

Building
------------

All project could be built both with Eclipse and make as well.

### TempestSDR library

Enter the folder and type

    make all
	
This will produce the library which could be found in the bin subdir. The headers you need to interface with it are located in src/include.

### Plugins

Go into a plugin directory and type

    make all
	
This should work unless there is something specific for the plugin itself. Look for a README in this case.

### JavaGUI

This is the Java wrapper and GUI. It builds all projects and supported plugins including the Java GUI itself. Go into the JavaGUI folder and type in

    make all JAVA_HOME=path_to_jdk_installation

On Windows 8 this could look like

    make all JAVA_HOME=C:/PROGRA~2/Java/jdk1.7.0_45