Build
-----

    mvn clean install

To build for 32 bit on a 64 bit machine:

    mvn clean install -Dos.arch=i386

To cross-compile for Windows using [MinGW](http://www.mingw.org/) ([Mac version](http://crossgcc.rts-software.org/doku.php)) or [MinGW-w64](http://mingw-w64.sourceforge.net/)
 -- also requires [Wine](http://www.winehq.org/) ([Mac version](http://code.google.com/p/darwine-builds/downloads/list)) for testing:

    mvn clean install -P cross-compile -Dhost.os=mingw32 -Dos.arch=i386

To install pkg-config on Mac OS X:

    brew install pkg-config
    sudo ln -s /usr/local/share/aclocal/pkg.m4 /usr/share/aclocal
