# CyanogenMod 11 (Android) on Toshiba AC100

This is an untracked fork of [android-installer](https://github.com/ac100-ru/android-installer), due to the restrictions of LFS. 

For more information about CyanogenMod for AC100 see [project page](https://paz00.ru/index.php/Android_4.0_installation).

## Installation

1. Clone this repository
2. Put `cm_ac100-ota-11.0-20140322-UNOFFICIAL.zip`, `gapps-4.4.2_20<200b>140110.zip`, `recovery-11.0-20140322.img` and `installer` files into the **root folder** of SD card or USB flash drive (first partition). Don't foget to safely remove the SD card/USB flash drive from a PC.
3. Start AC100 in recovery mode by holding `Ctrl+ESC` keys while pressing Power during boot.
4. Connect AC100 to your computer with USB-mini cable
5. Flash uboot onto device (must be root):

```
sudo ./nvflash --bl sos-uboot-r5-2014-07-01.bin --go
```

6. Insert the SD card/USB flash drive into AC100
7. Mount source:

```
mount /dev/sda1 /mnt
```

9. Run the installer:

```
sh /mnt/installer
```
