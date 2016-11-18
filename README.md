# Poisontap Antidote

Quick and dirty fix to defend against [Poisontap](https://samy.pl/poisontap/) 
  
Linux udev setup to block USB ethernet devices that don't have their MAC addresses listed in a static file.
  
Solutions for MacOSX and Windows welcome.

## Linux Install
```
install -m 755 -o root match_usb_network_device /usr/local/bin/match_usb_network_device
install -m 644 -o root anti-poisontap.rules /etc/udev/rules.d/zzz_anti-poisontap.rules
install -m 644 -o root usb_network_devices /etc/usb_network_devices

udevadm control --reload
```

## References
* [Poisontap](https://samy.pl/poisontap/) 
* [Linux udev](https://www.kernel.org/pub/linux/utils/kernel/hotplug/udev/udev.html)
* [Linux Kernel USB Authorization](https://www.kernel.org/doc/Documentation/usb/authorization.txt)


