[![Build Status](https://travis-ci.org/victoriarobotics/victoria_bringup.svg?branch=master)](https://travis-ci.org/victoriarobotics/victoria_bringup)
# victoria_bringup
Scripts to run when the system is turned on.

## GPSD
gpsd is used to provide fix data to the ROS gpsd-client.
It needs to be configured to look at the correct serial port on boot up.
The configuration file is
```
/etc/default/gpsd
```

For example, to have gpsd auto start, allow hot plugging, and always use 
`/dev/ttyUSB0`, edit the file to be:

```
START_DAEMON="true"
USBAUTO="true"
DEVICES="/dev/ttyUSB0"
```

We also need a udev rule.
