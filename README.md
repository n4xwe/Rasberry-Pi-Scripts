# RPi-Scripts
BASH Scripts that Install Ham Radio Software on the Raspberry Pi

These BASH scripts install either GNU Radio, WSJT-X, PiHPSDR, Fldigi, FreeDV, tweaktime or qsstv on a Raspberry Pi using the Raspberry Pi (fomerly Raspbian) Operating System. The scripts titled rpi-(name of the package) have been tested on an 8GB RPi 4 running the May 7, 2021, release of the Raspberry Pi OS 32-bit version. The scripts titled rpi-bullseye-(name of the package) have been tested on an 8GB RPi 4 running the January 28, 2022, release of the Raspberry Pi OS 32-bit version. The scripts titled rpi-mate-(name of the package) have been tested on an 8GB RPi 4 running the 64-bit version of Ubuntu MATE 20.10. The scripts titled rpi-ubuntu-(name of the package) have been tested on an 8GB RPi 4 running the of Ubuntu 21.04 ARM 64-bit version. They may or may not work successfully on other models of the Raspberry Pi or other versions of the Raspberry Pi OS, Ubuntu ARM or Ubuntu MATE Operating Systems.  

In order for the script to function correctly you must have a reasonable connection to the Internet.  The suggested method of launching the scripts is to create a separate directory named src off of the $HOME directory (/home/pi/src).  Copy the script file to the src directory.  Using the Command Line change the file permissions of the script to allow its execution (chmod +x name-of-the script.sh).  The same result can be achieved on the Desktop by doing a right click on your script and choosing Properties from the pop-up menu, then switch to the Permissions tab, opposite "Execute" change Nobody to Anyone.  To start the script from the Command Line preface the script name with a dot slash (./name-of-the-script.sh) and press the Enter key.  

The script will update all of the packages on your Operating System to their latest versions.  It will also locate, download and compile all of the required dependencies and the requisite source code.  In many instances there are statements in the scripts that place icons on the Desktop and provide essential configuration of the software.  In the case of GNU Radio the script installs two Python configuration statements but the OS must be rebooted to enable them.  

All of the scripts have detailed inline comments that explain the function of every line in the script.  They are offered under GPL v3.0 and can be easily modified by any user.  Approximate runtimes for the scripts are included in the script descriptions.  The exact runtime depends on a number of factors including the state of the packages on your system and the speed of your Internet connection.

PiHPSDR, by John Melton, G0ORX, is an excellent lightweight SDR Console that works with a variety of radios.  It uses the WDSP 1.18 library for signal processing, has the capability of implementing Puresignal adaptive pre-distortion, has an intuitive interface and is very stable. PiHPSDR interfaces with other programs through the Pulseaudio transport system.  There is a version of the script that supports the Rasbian OS and one that supports the Raspberry Pi flavor of Ubuntu Mate. The current release of PiHPSDR is 2.08-rc1. Script runtime time on a Raspberry Pi 4 is approximately 10 minutes.

GNU Radio, originally developed by Eric Blossom, K7GNU, and Matt Ettus, N2MJI, is a powerful DSP toolkit. It has a graphical interface that allows allows almost any DSP function to be performed on RF derived signals.  Script runtime on a Raspberry Pi 4 is roughly 2 hours and 30 minutes.  The rpi-mate-gnuradio3.8.2-grnet-digital_rf-osmosdr-hpsdr-setup.sh script was built for the HamSCI Tangerine-SDR project and works only on Ubuntu Mate 20.10 for the Raspberry Pi.  It installs GNU Radio 3.8.2 and builds the gr-grnet, gr-digital_rf, (limited) gr-osmosdr and gr-hpsdr blocks into the GNU Radio Companion. The rpi-gnuradio3.8.4-hpsdr script builds the 3.8.4 (latest as of 10/1/21) version of GNU Radio with the HPSDR source blocks. 

WSJT-X by Joe Taylor, K1JT, and currently supported by a group of very talented developers is weak signal software that includes, among other programs, FT8, FT4, JT8 and WSPR. The script also compiles the most recent version of the Hamlib library for integrated rig control,  Script runtime on a Raspberry Pi 4 is 35 minutes.

Fldigi by Dave Freese, W1HKJ and others is a digital mode console with integrated Hamlib rig control.  This console handles a multitude of digital modes including PSK-31, WeatherFax, Hellschreiber and CW.  The script installs Hamlib 4.4, fldigi 4.1.20, rigctl 1.4 and flwkeyer 1.2.3. Script runtime on a Raspberry Pi 4 is approximately 30 minutes.

FreeDV, by David Witten, KDØEAG, and David Rowe, VK5DGR, is a GUI client for Digital Voice. This script incorporates Codec2 and the LPCNet, neural network software. Script runtime on a Raspberry Pi 4 is approximately 10 minutes.

Dream is an AM/DRM software receiver written in C++ and Qt. Script runtime on a Raspberry Pi 4 is approximately 20 minutes

tweaktime, by Matt Roberts, KK5JY allows adjusting the system clock to provide accurate time synchronization for WSJT-X using the DT values in the WSJT-X GUI. Please take a look at kk5jy.net to find the instructions for using it.

qsstv is a digital or analog Slow Scan Television program with integrated Hamlib rig control. Script runtime on a Raspberry Pi 4 is approximately 30 minutes.
