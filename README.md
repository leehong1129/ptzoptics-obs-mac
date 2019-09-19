# OBS plugin for PTZOptics Camera Control

PTZOptics Camera Control is a plugin for the OBS (Open broadcaster Software) program.  This plugin allows you to control your PTZOptics camera via VISCA commands utilizing TCP.

### Prerequisites
. OBS Studio  
. This plugin is for 64bit based MacOS  

### Building
1. Configure using Cmake-Gui tool
2. Generate XCode project using Cmake-Gui tool
3. Include obs-module.h, obs-frontend-api.h, SDL.h headers (XCode -> obs-ptzcontroller -> Build Settings -> System Header Search Path)
4. Include SDL2 framework (XCode -> obs-ptzcontroller -> Build Settings -> Other Linker Flags ; XCode -> obs-ptzcontroller -> Build Settings -> Framework Search Path)
5. Build
6. After build should change the QtFramework install names
* install_name_tool -change @rpath/QtCore.framework/Versions/5/QtCore @rpath/QtCore obs-ptzcontroller.so

### Installing

1. Copy obs-ptzcontroller.so to Applications/OBS.app/Contents/Resources/plugins
2. Copy SDL2.framework to Applications/OBS.app/Contents/Frameworks/


