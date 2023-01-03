# Xbox 360 Neighbourhood
Xbox 360 Neighbourhood is a Windows shell extension included in the Xbox 360 SDK (XDK), that allows you to browse the HDD, remotely launch .xex files, take screenshots, etc. from your Windows PC.

Everywhere that references it tells you to download and install the XDK, the installer for which is 1.4gb and the installed size around 3gb.

If you only want Neighbourhood, that's a lot of wasted bandwidth/disk space. Surprisingly, I appear to be first person to extract the shell extension so it can be installed stand-alone (needing just 2.5mb of space).

## Info
The neighbourhood shell extension files come from XDK version v2.0.21256.3, the latest I am aware of. The registry entries were pieced together myself from an installed copy, with a few small tweaks (you can now rename the neighbourhood!). xbdm.xex came from somewhere on _the internet_, and I have no info on the author, version, etc.

This package has been tested and works fine on Windows 10 (x64), with both JTAG and RGH 360s running v2.0.17559.0 (latest).

## Installation

 1. Copy xbdm.xex to HDD1 on the 360, using your normal method.
 2. Configure dashlaunch to load the plugin (and reboot to enable it).
 3. On your PC, copy `xeshlext.dll` from `x32` or `x64` (according to your version of Windows) to `c:\windows\system32\`
 4. Run the `x360nhood-desktop.reg` or `x360nhood-network.reg` to merge into your registry. One adds the icon to the Desktop, the other to Network (if you want both, just run both reg files).
 5. Depending on your version of Windows, you may need to reboot (or at least restart explorer), Windows 10 does _not_ need this.
 
## Uninstall
1. Run `x360nhood-uninstall.reg` to remove the registry entries.
3. You will probably need to restart explorer, or even the PC, before step 3.
4. Delete `c:\windows\system32\xeshlext.dll`
