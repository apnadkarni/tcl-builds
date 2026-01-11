# tcl-builds

Experimental workflows for generating Tcl batteries-included distributions
using [BAWT](https://www.tcl3d.org/bawt/). Still very much a prototype. None
of the builds currently undergo testing. Nor are they verified or signed.
Please raise a ticket for issues and suggestions.

**Currently only 64-bit Tcl 9 builds are available. 32-bit or Tcl 8.6 builds TBD.**

The generated distributions can be downloaded from the 
[Releases](https://github.com/apnadkarni/tcl-builds/releases) page.

There is no installer. Distributions are ZIP archives. Extract and run.

Distributions include "stock" tclsh and wish, single file executables based
on both Tclkit and zipkits and a large number of packages, with some
differences between platforms.

## Windows

Windows distributions are built with MinGW gcc 14.2 and have been tested
on Windows 10.

## Linux

Built on Ubuntu-22.04 x64 and tested on my WSL system, once LD_LIBRARY_PATH
is configured to point to the extracted lib directory. Probably will not
work on older Ubuntu due to GLIBC requirements. No idea about other Linux
distributions.

## MacOS

MacOS builds use the `macos-latest` runner which is macOS 15 on ARM64. I
don't have a Mac so completely untested. No idea if the paths are
appropriate, whether it will work on older macOS versions etc.
Relationship with Marc Culler's signed builds needs to be
investigated to choose one or integrate in some form.

## Doing your own builds

To do your own builds, clone the repository. On the Actions page, click the
`Tcl/Tk Distribution` link on the left and then click the `Run workflow` button.
A pop-up shows the build options to select platform, Tcl version etc. The
built distributions will be downloadable from the Artifacts section of
the workflow run status page.

## Credits

All credit goes to Paul Obermeier for his [BAWT](https://www.tcl3d.org/bawt/)
framework which does 100% of the heavy lifting needed for building
distributions.

