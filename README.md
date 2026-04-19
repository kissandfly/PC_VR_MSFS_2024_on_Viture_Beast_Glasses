# PC VR Games / MSFS 2024 on Viture Beast glasses

A sum up of my journey to use the great Viture Beast glasses as a VR headset on a PC, mostly for MSFS 2024
Any improvments ideas very welcome...

## Install STEAM and SteamVR
To activate the null driver, you must edit two files in your SteamVR directory:
Null Driver Settings: Navigate to steamapps\common\SteamVR\drivers\null\resources\settings\default.vrsettings and change "enable": false to "enable": true. 
SteamVR Config: In resources\settings\default.vrsettings (or config\steamvr.vrsettings), set the following values:
"requireHmd": false
"forcedDriver": "null"
"activateMultipleDrivers": true

## Install VRto3D plugin
from https://github.com/oneup03/VRto3D
choose in default_config.json FOV adapted to glasses FOV 58 to 90

## Install OpenTrack for head tracking
from https://github.com/opentrack/opentrack
As it does not like glasses, adjust parameters to:
Input: NeuralNet Tracker / head-pose-0.2-big-onnx
Output : UDP over network (to SteamVR)

Optionals:
Camera : Resolution 640x480 ou 720p, Force FPS à 30-60, MJPEG activated 
FOV caméra : 56°
Filter : ROI Filter Alpha à 0.7 , Deadzone 1.0-1.5mm, Internal Filter activated
Threads : 1-2
Airtrack seems to work well too: https://github.com/AIRLegend/aitrack
