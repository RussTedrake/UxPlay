This project is an early stage prototype of unix AirPlay server.
Work is based on https://github.com/FD-/RPiPlay.
Tested on Ubuntu 19.10 desktop.
5G Wifi connection is the must.

Features:
1. Based on Gstreamer.
1. Video and audio are supported out of the box.
3. Gstreamer decoding is plugin agnostic. Uses accelerated decoders if availible. VAAPI is preferable.
4. Automatic screen orientation.

Building:
1. sudo apt-get install cmake
2. sudo apt-get install libssl-dev libavahi-compat-libdnssd-dev libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev gstreamer1.0-libav
NOT: 3. sudo apt-get install gstreamer1.0-vaapi (For Intel graphics)
3.5. Install from upstream RpiPlay instructions (but not gstreamer1.0-vaapi, which caused my gnome session to exit)
4. mkdir build
5. cd build
6. cmake ..
7. make
