Huawei Ascent P6 3.0.8 Kernel
=============================


Source:

Ascend P6 Open Source(P6-U06,JellyBean,kernel-3.0.8)

Features:

First Build
Only Added "Optimize for size" (so that the kernel should work without problems)
More will come


Credits:


m!k3 (for the right download-link ^^)
Huawei (for releasing this source)
CNexus (for his wonderful Boot.img tools)
worstenbrood (for his Huawei Update Extractor)
raolleel (Building the kernels)
jimbo77 for testing B118/CN


Warning:

keep in mind : THIS IS A VERY EARLY BUILD

tell me which bugs are there, or if this doesn't work _B118CN is tested, but should wok on every Rom with unlocked BL

Only Works with Unlocked Bootloader, so you must have been on B118CN

Should work with B118CN

Should work with B125 if you were on B118Cn before

Could work with B111 if your Bootloader is not relocked when you flash B111 from B118CN
(only released because everyone said that the kernel is only for B111 [which I can't belive)



I am not responsible for bricking/destroying your phone. Custom kernels comes with no warranty.

Compile only on Linux :

cd (change to home dir)

mkdir android-kernel (make a folder for all the files)

cd android-kernel

git clone [URL WILL BE ADDED SOON)

cd kernel

export ARCH=arm (select architecture of your phone)
export SUBARCH=arm (select architecture of your phone)
export CROSS_COMPILE=../toolchain/arm-linux-androideabi-4.6/prebuilt/linux-x86_64/bin/arm-linux-androideabi- (tell the Kernel, where your compiler is)

make clean && make mrproper (to clean the source)
make hisi_k3v2oem1_defconfig ARCH=arm (to load the default config of your phone)
make menuconfig (configue the Kernel [dont change settings you don't know, or your kernel will not work)
make -j[number of your cpu-cores+1] ARCH=arm (This will start the process .. will take some time)
make ARCH=arm zImage 

Now you have your zImage 

Include of your zImage to boot.img :

Download the Rom you want to use (B118CN is recommendet)

extract the rom

Use Huawei-Update-Extractor to extract boot.img (I used Windows to do so, cause wine doesn't do the job)
(http://forum.xda-developers.com/showthread.php?t=2433454) [sometimes its called 09.boot.img .. then just rename it to boot.img]

Download (http://forum.xda-developers.com/showthread.php?t=2319018)
extract
copy your boot.img to this folder
chmod +x umkbootimg (to make it executable)
chmod +x mkbootimg (to make it executable)

./umkbootimg boot.img

rm zImage (remove the zImage file)

copy your zImage in this folder where the zImage from your boot.img was

./mkbootimg new_boot.img

now you have a boot.img with new kernel
just flash it via fastboot
