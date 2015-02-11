udev rule for panel controller
===

1. Plug in your panels controller
2. Type dmesg into the terminal, and find the serial number of your controller
3. Edit 99-panels_controller.rules to reflect that serial number
4. Move 99-panels_controller.rules to /etc/udev/rules.d (requires sudo)

serial ports
===

The rule assigns a symbolic link '/dev/ttyS101' to the controller. When starting PControl, enter '101' as the serial port number

SD media
===

Might need to format card as Fat32 using command:
??

When burning to SD card from PControl, enter the drive number as something like: "/media/1F90-CF40" (see what drives are under /media to find the right number, if it does not have "CF" in it, it may not be formatted"


Running Pcontrol
===

1. turn off panels, and controller
2. turn on panels
3. turn on controller
4. boot matlab
5. add the Matlab_Codes_Ubuntu_FvB directory + subfolders to your path
6. Run PControl

What I changed
===

Some files may not yet be hacked, but these steps should fix any offending files:

1. replace '\' with '/'
2. remove ':' when associated with a disk name
3. replace 'del' with 'rm', and 'copy' with 'cp', and use '-r' instead of '/Q' or '/Y'
4. replace 'dos' with 'system' (only necessary in some files)
5. ubuntu is case sensitive.. some files may need to be renamed, or the calls to them be changed to match the case sensitive name






