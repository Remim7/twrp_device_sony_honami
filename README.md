# TWRP for Sony Xperia Z1

Minimal tree to build TWRP in android-9.0

## Compile
export ALLOW_MISSING_DEPENDENCIES=true

export LC_ALL="C"

. build/envsetup.sh

lunch omni_honami-eng

make -j4 recoveryimage

## Compile

Since the FOTAKERNEL partition of Xperia Z1 is only 16MB, and the compiled TWRP is too large, it can only be used in the boot partition.

Command to flash the boot partition

fastboot flash boot recovery.img 

fastboot reboot

## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Quad-core (4x2.2 GHz Krait 400)
Chipset | Qualcomm MSM8974 Snapdragon 800
GPU     | Adreno 330
Memory  | 2 GB RAM
Shipped Android Version | 4.3
Storage | 16 GB
Battery | Li-ion 2300 mAh battery
Display | 1080 × 1920 pixels, 5.0 inches (~441 ppi pixel density)
Rear Camera  | Sony G Lens 20.7 MP 1/2.3" Exmor RS IMX220 back-side illuminated sensor
Front Camera | 2.2 MP


## Device picture

![Sony Xperia Z1](https://cdn2.gsmarena.com/vv/pics/sony/sony-xperia-z1-2.jpg)
