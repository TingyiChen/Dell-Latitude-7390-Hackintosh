# Dell Latitude 7390 Hackintosh OpenCore EFI

## Tested macOS Version

macOS Monterey 12.2

## System Configuration
- Intel i5 8350U
- Intel UHD 620
- Western Digital SN550 1T
- Intel AX210
- Thunderbolt 3
- Touchscreen
- Sierra Wireless EM7455

## What's working
 - [x] Audio 
  
 - [x] Headphone jack

 - [x] CPU Speedstep

 - [x] iGPU acceleration

 - [x] Battery Management

 - [x] Backlight

 - [x] Ethernet

 - [x] HDMI (4K30 Only)

 - [x] Sleep & Wake

 - [x] Trackpad(w/ gestures)

 - [x] Camera

 - [x] USB

 - [x] Sleep (Lid & Fn + Insert)

 - [x] WiFi (2.4 + 5GHz) & BT

 - [x] MicroSD card reader 

 - [x] Native hotkey support w/ Fn keys

 - [x] USB-C charging

 - [x] USB-C DP-Alt(4K60)

 - [x] Thunderbolt 3 DP Output(4K60)

 - [x] Thunderbolt 3 (partially w/ Hotplug) (See not working below)

## What's not working(I have found)
Touchscreen(driver is working but can't operate normally?)

After sleep&wake, USB-C including Thunderbolt will stop work(need nvm fw patch maybe,need further investigation)

Headphone microphone

## What's not tested yet
WWAN(Recognized by system but doesn't have sim card to test)

## Things needed before using this EFI
Run in OpenCore Grubshell.efi:

### DVMT:
setup_var 0x804 0x2

setup_var 0x805 0x3

### CFG Lock:
setup_var 0x52D 0x0