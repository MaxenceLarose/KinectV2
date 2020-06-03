# HOWTO - Install Project Requirements

The goal of this document is to explain how to install the project's requirements.

### 1. Kinect 2 SDK

1. The reason why the Kinect 2 Node.js library we are going to use only works on Windows machines is that it relies on the official **Kinect 2 SDK** that can only be installed to Windows machines. Go ahead, and install it first from [this page](https://www.microsoft.com/en-us/download/details.aspx?id=44561). 
2. Follow the instructions. You might want to restart your machine after this step. Please also note that in order to install the SDK you will need a **64bit Windows 8 or higher**. 

### 2. Node js

1. Next, you need **Node.js** installed in the Windows command line. The official Windows Installer can be downloaded from [nodejs.org](https://nodejs.org/en/download/).
2. Make sure the installation was successful by entering `node -v` into the command line. It will give you the version number of Node installed. You need at least version 0.11.3 for the Kinect 2 module to work.

### 3. Node-gyp

1. There are no precompiled binaries yet, so you need to have [node-gyp installed on your system](https://github.com/nodejs/node-gyp). You can install `node-gyp` using `npm` in the project root:

   ```
   $ npm install -g node-gyp
   ```

   Depending on your operating system, you will need to install:

   ### On Unix

   - Python v2.7, v3.5, v3.6, v3.7, or v3.8
   - `make`
   - A proper C/C++ compiler toolchain, like [GCC](https://gcc.gnu.org/)

   ### On macOS

   - Python v2.7, v3.5, v3.6, v3.7, or v3.8
   - Xcode
     - You also need to install the `XCode Command Line Tools` by running `xcode-select --install`. Alternatively, if you already have the full Xcode installed, you can find them under the menu `Xcode -> Open Developer Tool -> More Developer Tools...`. This step will install `clang`, `clang++`, and `make`.
   - If your Mac has been *upgraded* to macOS Catalina (10.15), please read [macOS_Catalina.md](https://github.com/nodejs/node-gyp/blob/master/macOS_Catalina.md).

   ### On Windows

   Install tools and configuration manually:

   - Install Visual C++ Build Environment: [Visual Studio Build Tools](https://my.visualstudio.com/Downloads?q=Visual%20Studio%202017) (using "Build Tools for Visual Studio 2017 (version 15.9)" workload).
   - Launch cmd, `npm config set msvs_version 2017`

   If the above steps didn't work for you, please visit [Microsoft's Node.js Guidelines for Windows](https://github.com/Microsoft/nodejs-guidelines/blob/master/windows-environment.md#compiling-native-addon-modules) for additional tips.

### 4. Npm Install

1. Install the project's dependencies with the following command:

   ```
   $ npm install
   ```