# hid-backport

This repo contains a backport of the USB HID fixes in kernel versions 5.15 for systems where the kernel version is 5.10 <= version < 5.15.

The custom kernel module fixes compatibility issues in pre-boot for OS X systems.

## Compiling

To compile the modified kernel module, run the following commands:

```bash
# Install requirements
sudo apt install \
  -y \
  gcc-arm-linux-gnueabihf \
  bc \
  bison \
  flex \
  git \
  libssl-dev \
  libc6-dev \
  libncurses5-dev \
  make

./compile-module
```

After the script completes, it will place the compiled module under `bin/usb_f_hid.ko`.
