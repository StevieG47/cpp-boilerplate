# C++ Boilerplate
[![Build Status](https://travis-ci.org/dpiet/cpp-boilerplate.svg?branch=master)](https://travis-ci.org/dpiet/cpp-boilerplate)
[![Coverage Status](https://coveralls.io/repos/github/dpiet/cpp-boilerplate/badge.svg?branch=master)](https://coveralls.io/github/dpiet/cpp-boilerplate?branch=master)
---

## Overview

Simple starter C++ project with:

- cmake
- googletest

## Installation

- Checkout the repo (and submodules)
```
$ git clone --recursive https://github.com/dpiet/cpp-boilerplate.git
```

## Import into Eclipse
To import project into Eclipse:

Open Eclipse

Project --> Uncheck Build Automatically

File --> Import --> General --> Existing Projects into Workspace --> Next 

Select root directory --> Browse

Choose the *import* directory from cloned repository and hit Ok. This directory contains .project and .cproject files needed for Eclipse.  Hit Finish.

Files can be seen by going through the project tree.

The import directory was created with:
```
mkdir import
cd import
cmake -G "Eclipse CDT4 - Unix Makefiles" -DCMAKE_BUILD_TYPE=Debug -DCMAKE_ECLIPSE_GENERATE_SOURCE_PROJECT=TRUE ..
```



## Building in Eclipse

Click on the project in the project tree and use the Build All button on the tool bar to build the project. This can also be done with Ctrl+B.



## Running in Eclipse
In the project tree, right click the project and navigate to Run As --> Local C/C++ Application. Select the binary to run and hit Ok.

This can be also done by hitting the small arrow button directly right of the large green Run button on the toolbar, and then selecting the binary to run.



## Debug in Eclipse
In the project tree, right click the project and navigate to Debug As --> Local C/C++ Application, then choose which binary you want and hit Ok. If asked to open the Debug perspective hit yes. 

Like with running, this can also be done from the tool bar by hitting the small arrow next to the bug shaped Debug button and selecting the binary. 

Breakpoints can be set by double clicking on the wanted line when viewing the source code, and will be seen with a blue marker when it has been set. The toolbar can be used to resume the debug, terminate, and disconnect while debugging. To close the Debug perspective, go to Window --> Perspective -> Close Perspective.



## CppChEclipse
To use cppcheck in Eclipse go to Help --> Eclipse Marketplace

In the search tab, search for "cppcheclipse" then hit install.

Once installed, go to Window --> Preferences --> C/C++ --> cppcheclipse. In the cppcheck binary path, enter */usr/bin/cppcheck.* In cppcheclipse --> Problems, add/remove wanted/unwanted problems to check. More settings including specifying C++ version can be done in cppheclipse --> Settings.

cppcheck can be run by right clicking the project in the project tree and navigating to cppcheck --> Run cppcheck.



## Google C++ Style Guide
To follow Google C++ Style Guide, download the xml file from [here](https://raw.githubusercontent.com/google/styleguide/gh-pages/eclipse-cpp-google-style.xml) or in the command line ```wget https://raw.githubusercontent.com/google/styleguide/gh-pages/eclipse-cpp-google-style.xml```

To import into Eclipse, go to Window --> Preferences --> C/C++ --> Code Style --> Formatter

Click import and select the xml file, hit Ok. This changes the active profile to Google C++.

The formatter can be used with every save by going to Window --> Preferences --> C/C++ --> Editor --> Save Actions

Check *Format source code* and choose Format all lines or Format edited lines, then hit Ok. To manually format a line, right click and go to Source --> Format and select *The statement on the current line*
