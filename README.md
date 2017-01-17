# ElectricSheepRedux
Continuation of the epic ElectricSheep project

Current development is done on Ubuntu 16.04 



# Install

1. apt-get install subversion autoconf libtool libgtk2.0-dev libgl1-mesa-dev libavcodec-dev libavformat-dev libswscale-dev liblua5.1-0-dev libcurl4-openssl-dev libxml2-dev libjpeg8-dev libgtop2-dev libboost-dev libboost-filesystem-dev libboost-thread-dev libtinyxml-dev freeglut3-dev glee-dev wx3.0-headers libwxgtk3.0-dev  wx3.0-headers

2. Setup Ubuntu Screensaver
 1. sudo apt-get remove gnome-screensaver
 2. sudo apt-get install xscreensaver xscreensaver-data-extra xscreensaver-gl-extra

3. Build flam3
 1. automake --add-missing
 2. ./configure
 3. make install
 
4. Build ES
 1. ./configure
 2. make
 3. make install
 
5. Add ESR to xscreensaver
 1. vim ~/.xscreensaver and change:
```
                                testx11 -root                               \n\
  GL:                           electricsheep -root 1                       \n\



pointerPollTime:    0:00:05
pointerHysteresis:  10
```

to:
```
  GL:                           splitflap -root                             \n\
                                testx11 -root                               \n\
  GL:                           electricsheep -root 1                       \n\



pointerPollTime:    0:00:05
pointerHysteresis:  10
``` 

#To Do
