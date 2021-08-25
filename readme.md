What's this?
==========

This is a forked alternative to _xinput_calibrator_ (as seen on
[github](https://github.com/tias/xinput_calibrator),
[FreeDesktop](https://www.freedesktop.org/wiki/Software/xinput_calibrator/),
[Ubuntu](https://packages.ubuntu.com/disco/xinput-calibrator), etc.).

Similarities:
- For Unix-like OS
- Calibrates touchscreens

Differences:

|Thing           |xinput_calibrator                |xcalibrate                     |
|----------------|---------------------------------|-------------------------------|
| Language       |C++                              |Python3                        |
| LOC            |2,289                            |284                            |
| Interface      |Command-line args with some GUI  |Walkthrough-based with some GUI|
| GUI toolkit    |X                                |tk                             |
| Cal points     |4                                |Selectable                     |
| Math           |Manual                           |Numpy least-squares            |
| Outputs        |Xorg.conf, hal, xinput           |xinput                         |
| Popularity     |High                             |Zero so far                    |
| Tested         |Pretty well                      |Not very well                  |
| OS distribution|Available in most major repos    |WINEdows                       |
| Dependencies   |libstdc++, libx11, libxi         |python3, tkinter, numpy        |

_xinput_calibrator_ features precalibration, timeouts, misclick detection, fake driver testing, and
a resizable window.
_xcalibrate_ features none of those things, but offers some other features not present in
_xinput_calibrator_, including pre-save cal test, cal quality indicator, arbitrary cal point count,
and a slightly more informative GUI. Also, the source is quite simpler.

Why this fork?
=========
While reinderien's calibration tool is excellent, however, this script wouldn't work on my personal CF-19 laptop, since the touchscreen shows up as a keyboard device.
This fork has been modified to show BOTH keyboard and pointer devices in the selection now.
It is also modified to actually save the .conf file in the correct directory automatically (instead of having to mess around running text editors in root and saving changes manually).
This does however mean the script needs to be run as sudo.

How to install?
=========
First you need the dependencies
	apt install python3-tk python3-numpy
	
You can then run: 
	sudo python3 xcalibrate.py
To calibrate the display
	
Optionally copy the xcalibrate.py file to /usr/bin/
Then copy the .launcher file to /usr/share/applications/

