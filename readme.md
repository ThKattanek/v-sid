# realSID
## This is a SID emulator with a simply sequenzer (The project was for my technician study)
### [Latest version here](https://github.com/ThKattanek/realsid/releases/latest)

## Screenshot
![Screenshot](screenshot.png)

## Used libraries
* Qt4
* SDL
* SDL_gfx

## Build
```bash
git clone https://github.com/ThKattanek/realsid.git
cd realsid
mkdir build
cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make
make install
```
Optionaly -DCMAKE_INSTALL_PREFIX=[InstallPfad] can be used.

## Uninstall
```bash
xargs rm < install_manifest.txt
```
Warning! Directories created by the installation are not removed, but only all files created.

## Compiling for Windows x32 with MXE (Crossdev)
```bash
cd ~
git clone https://github.com/ThKattanek/realsid.git
cd realsid
mkdir build-win-x32
cd build-win-x32
[MXE-PATH]/usr/bin/i686-w64-mingw32.static-cmake .. -DWIN32_STATIC_BUILD=TRUE -DCMAKE_INSTALL_PREFIX=../install-win-x32
make
make install
```
## Compiling for Windows x64 with MXE (Crossdev)
```bash
cd ~
git clone https://github.com/ThKattanek/realsid.git
cd realsid
mkdir build-win-x64
cd build-win-x64
[MXE-PATH]/usr/bin/x86_64-w64-mingw32.static-cmake .. -DWIN32_STATIC_BUILD=TRUE -DCMAKE_INSTALL_PREFIX=../install-win-x64
make
make install
```
## Complete build and create the windows versions (32/64bit) as 7zip with Script (crossbuild-win-releases.sh)
#### MXE required
```bash
cd ~
git clone https://github.com/ThKattanek/realsid.git
cd realsid
./crossbuild-win-releases.sh [MXE-PATH]
```
### [MXE Website](http://mxe.cc)
