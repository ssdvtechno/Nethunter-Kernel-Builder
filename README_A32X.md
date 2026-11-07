# A32 5G NetHunter build

This builder is configured for Samsung Galaxy A32 5G SM-A326B on Android 13.

- Kernel source: `revx0012/android_kernel_samsung_a32_5g`, branch `ksu-susfs`
- Base kernel: 4.14.186-27095505 with KernelSU-Next and SUSFS already integrated
- Defconfig: `a32x_defconfig`
- NetHunter changes: Kali 4.14 Wi-Fi injection behavior adapted to this source branch, plus a config fragment for USB HID/gadget functions, Bluetooth, USB networking, and common external Wi-Fi adapters
- Build output: GitHub Actions artifacts, including an AnyKernel3 zip for SM-A326B

The release zip and `ksu_susfs` binary in the parent folder are prebuilt release assets, not kernel source. The build fetches source from the kernel repository. `ksu_susfs` remains a separate userspace utility.

## Run the build

Push this modified working tree to your fork of `Nophere1/Nethunter-Kernel-Builder`, then run **Actions → Build kernels → Run workflow**.