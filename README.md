# !WIP!

## NetHunter MIX3

Попытка сделать свой постремонтный MIX3 с левым экраном опять нужным устройством.

### Список исходников

Список требующегося

1. `git clone https://github.com/ROMSDEV/android_kernel_xiaomi_sdm845`
2. `git clone https://github.com/ROMSDEV/device_xiaomi_sdm845-common`
3. `git clone https://github.com/ROMSDEV/device_xiaomi_perseus`
4. `git clone https://gitlab.com/the-muppets/proprietary_vendor_xiaomi`
   ```text
     - AndroPlus-org/vendor_xiaomi DMCA
     - TheMuppets/proprietary_vendor_xiaomi DMCA
     - M1cha/proprietary_vendor_xiaomi DMCA
   ```
5. 

### Сборка тестового ядра.
ждя 64-битных
```
git clone https://android.googlesource.com/platform/prebuilts/gcc/linux-x86/aarch64/aarch64-linux-android-4.9 -b android10-release toolchain64
export ARCH=arm64
export SUBARCH=arm64
export CROSS_COMPILE=`pwd`/toolchain64/bin/aarch64-linux-android-
make your_device_codename                         
make -j$(nproc)
```

### Сборщик ядра

```shell
git clone https://gitlab.com/kalilinux/nethunter/build-scripts/kali-nethunter-kernel; cd kali-nethunter-kernel
cp local.config.examples/local.config.example.sdm660 local.config; ./build.sh
```
