# NAME  
pylight - A simple backlight controller written in Python.  

# DESCRIPTION  
`pylight` is a simple software written in Python to control backlights and other lights on GNU/Linux system with `xbacklight`-like options.
`pylight` works in a fully CLI environment, which does not require X to be running while `xbacklight` does.  

# INSTALLATION
First, clone `pylight` repository.  
``` sh
$ git clone https://github.com/akihironitta/pylight.git
$ cd pylight
```

To enable `pylight` running without root permission, place `90-backlight.rules` in one of the udev rules directories, e.g. `/etc/udev/rules.d/`.  
``` sh
$ mv 90-backlight.rules /etc/udev/rules.d/
```

Rebooting the system may be required to apply this configuration depending on your system.  
``` sh
$ sudo reboot
```

# OPTIONS
- `-max` set brightness to maximum value  
- `-min` set brightness to minimum value (a quater of maximum value)  
- `-set` set brightness to value  
- `-inc` increase brightness by value  
- `-dec` decrease brightness by value  

# Usage
Check the current brightness.  
``` sh
pylight
```

Set to the specified brightness `100`.  
``` sh
pylight -set 100
```

Set to the maximum brightness.  
``` sh
pylight -max
```

Set to the minimum brightness.  
``` sh
pylight -min
```

# SEE ALSO
- [[https://github.com/tcatm/xbacklight][xbacklight]]  

