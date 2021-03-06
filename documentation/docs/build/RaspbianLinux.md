# Build Instructions for Raspbian Linux (Jessie)

## Requirements

Please install the following packages via

   `sudo apt-get install git`<br/>
   `sudo apt-get install cmake`<br/>
   `sudo apt-get install root-system`<br/>
   `sudo apt-get install gcc`<br/>
   `sudo apt-get install locate`<br/>
   `sudo apt-get install libqt4-dev`<br/>
   `sudo apt-get install libqwtplot3d-qt4-dev`<br/>
   `sudo apt-get install libgphoto2-dev`<br/>
   `sudo apt-get install libexiv2-dev`<br/>
   `sudo apt-get install libopencv-dev`<br/>
   `sudo apt-get install pkg-config`<br/>
   `sudo apt-get install libboost-dev`<br/>
   `sudo apt-get install arduino`<br/>
   `sudo apt-get install arduino-mk`<br/>
   `sudo apt-get install libcurl4-openssl-dev`

The software relies on a newer version of `qwt` (>=6.1). In order to install this
newer version, edit the file
`sudo pico /etc/apt/sources.list` and add the line

   `deb http://archive.raspbian.org/raspbian/ testing main contrib non-free rpi`

to its end. After that execute

   `sudo apt-get update`

You can now install `qwt` via

   `sudo apt-get install libqt4-dev`<br/>

You should now comment out the line previously added to `/etc/apt/sources.list`
and run 

   `sudo apt-get update`

## Building

Go to the directory to which you checked out the source code and run

   `./configure` [options]

with options as described in the [documentation](./configure).

Then run

   `source tkmodlabenv.sh`
   
in case you use `bash` or add the script to your `.bashrc`. You should
now be good to go and build the software by running

   `make`
