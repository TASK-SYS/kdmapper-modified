#KDMapper Modified

![C++](https://img.shields.io/badge/C%2B%2B-17-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-lightgrey.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

A modified version of the popular **kdmapper**, optimized for modern game environments and enhanced stability. This tool utilizes the `iqmwan64.sys` Kernel driver vulnerability to manually map non-signed & signed drivers into kernel memory.

## 🚀 Enhancements
- **Reduced Detection Footprint:** Modified string encryption and entry point obfuscation to evade basic pattern scanning.
- **Improved Cleaning:** Enhanced clearing of `PiDDBCacheTable` and `MmUnloadedDrivers` to minimize traces left in the kernel.
- **Mdl Support:** Added optional MDL mapping for better stability with certain system configurations.
- **Custom Parameter Passing:** Allows passing custom data to the driver entry point more efficiently.

## 🛠 Usage

> **Warning**: Use this tool at your own risk. Loading unsigned drivers can cause System BSODs if the driver is not properly written for kernel standards.

1. Ensure your driver is compiled as a `.sys` file with **Control Flow Guard (CFG)** disabled.
2. Run the mapper via command line:
   ```cmd
   kdmapper.exe your_driver.sys
