
# Infos and Links for CAN bus communication in Linux Systems

### Basics
https://elinux.org/CAN_Bus

### socketCAN


### Script for adding virtual CAN interface (vcan) 
```shell
#!/bin/bash
# Make sure the script runs with super user privileges.
[ "$UID" -eq 0 ] || exec sudo bash "$0" "$@"
# Load the kernel module.
modprobe vcan
# Create the virtual CAN interface.
ip link add dev vcan0 type vcan
# Bring the virtual CAN interface online.
ip link set up vcan0
```
