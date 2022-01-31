# 32 bit EFI files

Some older computers only support the 32 bit EFI boot.
One of them is the MacBook 2007. Although it can run a 64 bit OS,
it only supports 32 bit EFI boot partitions.

# Example
If you want to install Ubuntu on a MacBook 2007, you can not
just use the USB installer that comes with it.

To make it work:
1. Flash the Ubuntu USB installer on a USB. msdos partition table seemed to work fine.
2. Copy content of this repository into that installer USB
3. Don't install Ubuntu but first try it on the USB so we can install an additional package missing.
4. Run the following commands to install grub 32 bit package so that the installation will be succesful at the end.
```
sudo apt-get update
sudo apt-get install grub-efi-ia32
```
5. Now install Ubuntu and it will work.

Well, it did for me :)
