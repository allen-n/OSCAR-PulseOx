# OSCAR-PulseOx
Modifications of OSCAR to streamline pulseox data manipulation (https://www.sleepfiles.com/OSCAR/)

---------------------
OpenSource CPAP Analysis Reporter - OSCAR

OSCAR is a derivative of SleepyHead version 1.1.0,created when that was abandoned by Mark Watkins.

SleepyHead was a cross platform, opensource sleep tracking program for reviewing CPAP and Oximetry data,
which are devices used in the treatment of Sleep Disorders like Obstructive Sleep Apnea. It was released
under the GPL version 3 license. See the file COPYING for those details.

SleepyHead was written by Mark Watkins (aka Jedimark), an Australian software developer afflicted with sleep apnea.

SleepyHead was copyright (C) 2011-2018 by Mark Watkins <mark@jedimark.net>

Portions of OSCAR are copyright (c) 2019 by Nightowl Software <michaelnightowl99@gmail.com>

Requirements: (Linux package names are given, Windows and Mac should be similar)
-------------
Qt5.9 SDK with help (Qt5.9 from http://qt.io/download-open-source recommended)
The help modules are libqt5help5, qttools5-dev and qttools5-dev-tools

Qt5.7 SDK without help is possible (for Debian Stretch)

All systems need qtcreator or qttools5-dev-tools

All systems need qt5-default, libqt5serialport5, libqt5serailport5-dev and libqt5opengl5-dev
Linux also needs libudev-dev and zlib1g-dev

OSX needs Xcode and commandline tools from AppStore,

Windows needs MinGW (in Qt5 SDK) or VC++2015 Community, and a matching set of Qt libraries.

Building:
--------

Recommend shadow building to not cruft up the source code folder:

cd ..
mkdir build
cd build
qmake ../OSCAR-code/OSCAR_QT.pro 
make

You may need to add a -spec option to qmake to suit your platform. 
Adding -j4 speeds up the make command on a dual core or greater system.

Building on OSX:
---------------
Build as above. If qmake fails with the error:
Project ERROR: Xcode not set up properly. You may need to confirm the license agreement by running /usr/bin/xcodebuild
edit the file: 
QT_INSTALL_DIR/5.9/clang_64/mkspecs/features/mac/default_pre.prf

and replace
/usr/bin/xcrun -find xcrun 2>/dev/null

with
/usr/bin/xcrun -find xcodebuild 2>/dev/null



Software Licensing Information
------------------------------
OSCAR is released under the GNU GPL v3 License. Please see below for a note on giving correct attribution
in redistribution of derivatives.

It is built using Qt SDK (Open Source Edition), available from http://qt.io.

Redistribution of derivatives ( a note added by Mark Watins )
-----------------------------
Mark Watkins created this software to help lessen the exploitation of others. Seeing his work being used to exploit others
is incredibly un-motivational, and incredibly disrespectful of all the work he put into this project.

If you plan on reselling any derivatives of SleepyHead, I specifically request that you give due credit and
link back, mentioning clearly in your advertising material, software installer and about screens that your
derivative "is based on the free and open-source software SleepyHead available from http://sleepyhead.jedimark.net,
developed and copyright by Mark Watkins (C) 2011-2018."

It is not enough to reference that your derivative "is based on GPL software".

