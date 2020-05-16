# TelescopeTracker

_**Please note: this is work in progress and not a finished product**_

The goal of this project is to create a Raspberry Pi based telescope star tracker.
It uses the Raspberry Pi hq camera to fit a 1.25inch eyepiece holder, connect to a pc using buildin wifi to connect to PHD2 or alike by simulating a webcam.

![](https://github.com/LennartKlaver/TelescopeTracker/tree/master/Assembly/IMG_0430.jpg)
![](https://github.com/LennartKlaver/TelescopeTracker/tree/master/Assembly/IMG_0404.jpg)

# Parts
* A 3d printed camera mount for the eyepiece.
* A Raspberry Pi. https://www.raspberrypi.org/products/
* A nice casing to fit the raspberry in.
* A Raspberry Pi hq camera: https://www.raspberrypi.org/products/raspberry-pi-high-quality-camera/
* 4 M3x25 hexagon machine screw with cilinder head.
* 8 M3 nuts (I used self locking nuts to make sure they do not come loose).

# Instructions

## Assembly
1. Download the STL file and 3d print it.
2. From the camera, remove the small part that can be used to screw the cam on a mount. It is fixed by 2 hex bolts.
3. Check if the camera fits your print.
4. Place the printed part on top of the raspberry casing and mark the 4 holes.
	Please pick a spot where there are no components underneath (not to close to the usb ports).
	Also take note for the orientation of the ribbon cable. My casing had some room above the usb port so I guided the cable to that side.
5. Drill the mounting holes with a 3mm drill (remove the raspberry pi from the casing before drilling ... ).
6. Screw 4 M3x25 hexagon screws in the printed casing.
7. Push the camera module gently in its place. Sometimes it fits perfect, sometimes you have to turn the screws. Please apply proper ESD protection
8. Fixate the camera with 4 nuts..
9. Place the camera on top of the raspberry casing, do not forget the cable.
10. File a small gap to fit the ribbon cable inside the raspi casing.
11. Close the raspberry pi casing.
12. Place the camera on your telescope and power it up.

## Software
From here I assume you know a little bit about Raspberry Pi's. I used a headless setup and use SSH to communicate with the platform.
I connected the camera with my wifi and then used the steps below.
1. To enable the camera follow these steps: https://www.raspberrypi.org/documentation/usage/camera/
2. Check if the camera works by a call from the terminal: `raspistill -o testshot.jpg`
	Please note: if the image looks blurry, you need to focus the telescope/camera.
3. Install the RPi web interface for easy looking by browsing to the RasPi IP address: https://elinux.org/RPi-Cam-Web-Interface
	1. `sudo apt-get update`
	2. `sudo apt-get dist-upgrade`
	3. `sudo apt-get install git` 
	4. `git clone https://github.com/silvanmelchior/RPi_Cam_Web_Interface.git`
	5. `cd RPi_Cam_Web_Interface`
	6. `./install.sh`
	7. Browse to the Raspberry Pi's ip address and see the camera output.
	
To be continued....

# Development
## Finished
* Hardware design finished.
* Casing design finished.
* The camera mount fits the eyepiece.
* The camera works.
* The Raspberry Pi streams video with minimal delay.

## Next step
* Integrate the stream into windows cam system.
	