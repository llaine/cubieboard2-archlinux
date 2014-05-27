cubie2-arch
===========

# Installation 

[From Nwgat](http://nwgat.net/easily-install-arch-linux-on-your-cubieboard2/)

[Script from edwardoid](https://github.com/edwardoid/cubieboard-arch-installer)

__Linux system required__

### Formating the SdCard

1. Open `gParted`
2. Make the first partition in `Ext4` with the full size of your sd card. And let 16 MB Free
3. Make the second partition of `16 M` in `Fat16`

### Creating the bootable SD CARD

1. You can follow the [official arch installation tutorial](http://archlinuxarm.org/platforms/armv7/allwinner/cubieboard-2)
2. Or download and launch this script 
3. `wget https://raw.githubusercontent.com/edwardoid/cubieboard-arch-installer/master/install_arch_linux_-_cubieboard2.sh`

### Managing the script 

1. Find your sdcard with `df -h`
2. Launch the script, follow the instruction. 

### Connecting to the cubie 

1. By default arch linux doesn't output with HDMI, you can enable [it](http://archlinuxarm.org/forum/viewtopic.php?f=33&t=7215). 
2. Or connect to ssh. 
3. Find your cubie's IP with nmap or your router. 
4. `nmap -sP 192.160.0.0/24` 
5. Connect to ssh `ssh CUBIE_IP -l root` to default password is `root`


### Troubleshooting 

The name of the two partition of your card might be like `sdb0p1` and `sdb0p2`, in that case you need to change the line in the script adding a `p` before `1` (for example line 75 or 89)


Enjoy ! 

