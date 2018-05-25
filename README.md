# linux-4.9.57-i
After crash i created
=================================

Method 1.

>time make -j 12
>time make modules_install
>time make install
update-grub

///////////////////////////////////////////////////////////////////

Methdo 2. 

Pre-requirment
>sudo apt-get install gcc libncurses5-dev dpkg-dev

.config
>make menuconfig

compille 
>make -j 12 KDEB_PKGVERSION=1.CUSTOMENAME deb-pkg
//KDEB_PKGVERSION=$(make kernelversion)-1

install
>dpkg -i ../linux*.deb
>reboot

To list
>dpkg --list | grep linux-image
>dpkg --list | grep linux-headers

To remove
>sudo apt-get purge linux-image-3.19.0-15
>sudo apt-get purge linux-headers-3.19.0-15
//////////////////////////////////////////////////////////////////////////
http://ask.xmodulo.com/remove-kernel-images-ubuntu.html







