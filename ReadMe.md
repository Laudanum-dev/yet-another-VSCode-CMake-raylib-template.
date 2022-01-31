# VSCode + CMake raylib template.
This template will have bare minimum to be able to develop applications with raylib, using CMake as build tool, and VSCode as IDE for developing and debugging. Tested on Windows, should be working on any OS.  
The repo contains first example from raylib's core example catalog.

### Requirements
1) Have some general knowledge about CMake (https://cmake.org/cmake/help/latest/guide/tutorial/index.html)
2) Have some general knowledge how VSCode works (file 'launch.json', CMake extension, etc)
3) Have some general knowledge about C/C++ :^)
4) Download MinGW-w64 and install it (raylib won't work with just MinGW since it's kinda outdated). I used w64devkit version (https://github.com/skeeto/w64devkit/releases/tag/v1.10.0), in case you're struggling with installing from mingw-w64 own website.
5) Download CMake from it's website and install it
6) Clone repository (via green button above for example)
7) Open it in VSCode. Make sure that you have C/C++ and CMake + CMake Tools extensions installed (recommended)
8) You should be able to `F1 -> CMake: Configure` to install raylib and configure build files and then `F1 -> CMake: Build` to test out the building (result will be exe in build/ directory)

### How to run / debug
* Run without debugging: `Shift + F5`
* Run with debugging: `Ctrl + F5` / `F1 -> CMake: Debug`
* Release build: `F1 -> CMake: Select Variant -> Release` and then `F1 -> CMake: Build`. The result will be in build/ directory. __To be able to debug again__ you'll have to change configuration back to Debug (`F1 -> CMake: Select Variant -> Debug`)

### Example info on how to build
In case you are developing it with a team, or just making your project open source, some guide on how to build your app will be helpful. If you haven't done any changes to CMake files, the info above will be very actual.
---
1) Install CMake from their official website (https://cmake.org/)
2) Install C/C++ compiler
    2a) (Windows) Download MinGW-w64 from their official website (it might be complicated to do, easiest way so far is to download container'ed version from here https://github.com/skeeto/w64devkit/releases/tag/v1.10.0 (just download, extract, and put a path to it's bin folder into the PATH variable))
    2b) (Linux) Use any package manager you prefer (`sudo apt install build-essentials` for Ubuntu, `sudo pacman -S gcc` for Arch, anything like this)
3) Clone repository (via green button above -> Download ZIP -> Extract it somewhere, or `git clone \[your_project_url.git\])
4) Let's say that your repository is now at for example `C:/repository/`, in case it's not then just replace this path in later steps
5) Create inside the repository a folder called `build` (so it looks like `C:/repository/build/`)
6) Open command line 
7) Execute `cd C:/repository/build/`
8) Execute `cmake ..`
9) Execute `cmake --build .`
10) Built app will be at `C:/repository/build/`

#### Sources of information:
* raylib examples: https://www.raylib.com/examples.html
* raylib guide for using it with CMake https://github.com/raysan5/raylib/wiki/Working-with-CMake
* Extended CMakeLists from the guide above https://github.com/raysan5/raylib/blob/master/projects/CMake/CMakeLists.txt
* Debugging with CMake (and vscode) https://vector-of-bool.github.io/docs/vscode-cmake-tools/debugging.html
