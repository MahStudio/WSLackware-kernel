<p align="center">
  <img width="100" height="100" alt="WSLackware" src="./WSLackware/images/tux.png">
</p>

# Slackware's default kernel for WSLackware and other WSL2 distros

[WSLackware](https://github.com/Mohsens22/WSLackware/) is an unofficial version of Slackware for Windows Subsystem for Linux on Windows 10, 11 and Windows Server.

You can find more info about the project, downloading and installation here:
https://github.com/Mohsens22/WSLackware/

This is the default kernel 5.15.19 which is included in Slackware's latest stable release, customized to work with WSLackware
and other WSL2 distros.

You can download pre-built kernels from the [Releases](https://github.com/RezaT4795/WSLackware-kernel/releases).

Or you can proceed and build it from the source.

## IMPORTANT NOTE! READ BEFORE PROCEEDING
This is the first release of this kernel and it is considered as an ALPHA release.
It works fine on WSL2, but some features might NOT work, such as WSLg.

## Build Instructions
Instructions for building with a WSLackware distribution are
as follows:

1. Install the build dependencies (I recommend you to install all packages of d/ series which are development tools):  
   `$ sudo slackpkg install d`
2. Build the kernel using the pre-made kernel configuration:  
   `$ make KCONFIG_CONFIG=WSLackware/config`
   
Instructions for building with an Ubuntu distribution are
as follows:

1. Install the build dependencies:  
   `$ sudo apt install build-essential flex bison dwarves libssl-dev libelf-dev`
2. Build the kernel using the pre-made kernel configuration:  
   `$ make KCONFIG_CONFIG=WSLackware/config`

## Install instructions

Please see the documentation on the [.wslconfig configuration
file](https://docs.microsoft.com/en-us/windows/wsl/wsl-config#configure-global-options-with-wslconfig) for information on using a custom built kernel.


### Credits

- Linus Torvalds and all of the Linux community for making this kernel
- Microsoft for WSL2 and kernel patches

### Contributing

You can [send me issues](https://github.com/RezaT4795/WSLackware-kernel/issues) and let me know about bugs, missing features or anything that I need to know.
