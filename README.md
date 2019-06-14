# APC3710-IOT-edge
The APC3710 is a Consumer Edition board based on the i.MX6 series of SoCs. The i.MX 6 series of applications processors combines scalable platforms with broad levels of integration and power-efficient processing capabilities particularly suited to multimedia applications. The i.MX 6Quad processors feature advanced implementation of the quad ARM Cortex-A9 core, which operates at speeds up to 1.2 GHz. They include 2D and 3D graphics processors, 1080p video processing, and integrated power management. Each processor provides a 64-bit DDR3/DDR3L/LPDDR2 memory interface and a number of other interfaces for connecting peripherals, such as WLAN, Bluetooth, GPS, hard drive, displays, and camera sensors.
Specifications:
Processor
iMX6Q,Quad Cortex-A9@1.2 GHz
Memory/Storage
1GB LPDDR3 Memory
8GB eMMC5.1 Storage
Display	:
HDMI v1.4	x 1
LVDS Header   x1
Audio	:
Audio out	x1
Mic in   x1	
Connectivity:	
Gigabit Ethernet, 10/100/1000Mbps
WLAN 802.11 a/b/g/n/ac, 2.4G/5GHz
Bluetooth 4.1
Expansion connector:
USB 2.0 Host	x2		
USB 2.0 OTG	x1		
Mini PCIE Connector	x1
SATA Connector	x1	
SATA Power Connector	x1
CAN Bus Header	x1	
SPI Bus Header	x1	
UART Bus Header	x1	
External Storage			
Micro SD socket	x1	
User Interface			
Power/Reset


OS-support
Yocto

Install Yocto Steps.

Step1: connect APC3710 to Computuer via USB
Step2:  input command:  imx-yocto-flash.bat for downloading Yocto under serial port with Win10 64bit
Step3:  after finishing,  restart APC3710, then input the below command for installing.
setenv mmccargs  'sentenv bootargs ${bootargs} root=/dev/mmcblk3p2 rootwait rw video=mxcfb0:dev=hdmi 1920*1080M@60,if=RGB24'

