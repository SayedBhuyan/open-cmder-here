[Windows] "Open Cmder Here" in context menu

https://github.com/cmderdev/cmder.wiki.git

Note! If you wish to avoid manually fiddling with your registry, use the instructions in the README to setup a Shortcut to open Cmder in a chosen folder.
To add an entry in the Windows Explorer context menu to open Cmder in a specific directory, paste this into a OpenCmderHere.reg file and double-click to install it.

Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\Background\shell\Cmder]
@="Open Cmder Here"

[HKEY_CLASSES_ROOT\Directory\Background\shell\Cmder\command]
@=hex(2):25,00,43,00,4d,00,44,00,45,00,52,00,5f,00,49,00,4e,00,\
  53,00,54,00,41,00,4c,00,4c,00,5f,00,44,00,49,00,52,00,25,00,5c,00,43,00,6d,\
  00,64,00,65,00,72,00,2e,00,65,00,78,00,65,00,20,00,2f,00,53,00,54,00,41,00,\
  52,00,54,00,20,00,22,00,25,00,76,00,22,00,00,00


Then press the Windows + Pause keys to open the System Settings, go to Advanced Settings and add the Environment variable CMDER_INSTALL_DIR to point to the path of your installation.

System Settings Environment Variable English

After adding this, a restart of the PC/OS is required to make it work
© 2017 GitHub, Inc.