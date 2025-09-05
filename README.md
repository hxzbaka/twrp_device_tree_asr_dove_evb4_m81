### TWRP device tree for M81 (dove_evb4)

=========================================

The Redmi K50 (codenamed _"dove_evb4"_) is a high-end, mid-range smartphone from ASR.

It was released in 2025.

## Compile

First checkout minimal twrp with aosp tree:

```
repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
repo sync -j$(nproc --all)
```

Finally execute these:

```
source build/envsetup.sh
repopick <needed patch>
lunch twrp_dove_evb4-eng
mka vendorbootimage -j$(nproc --all)
```
## To use it:

```
fastboot flash vendor_boot out/target/product/dove_evb4/vendor_boot.img
```
