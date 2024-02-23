# FA506IV-OpenCore
OpenCore EFI for ASUS FA506IV hackintosh.

## Disclaimer
**All risks arising from the use of this project are solely your responsibility, and are not related to the project author or associated contributors.**

Reading the [Dortania Guide](https://dortania.github.io/OpenCore-Install-Guide/) before installing is highly recommended.

## FA506IV Specs

- AMD Ryzen 7 4800H
- AMD Radeon Vega Graphics
- 16GB DDR4 RAM
- NVIDIA RTX2060 6GB (Disabled)
- Intel 660p SSD 512GB
- Realtek RTL8822CE Wireless NIC (Disabled)
- Realtek Gigabit Ethernet

## Status

Tested on Ventura and Sonoma without major issue.

| Status |   Feature   |  Note |
| ------ |  ---------- | ------|
| ✅      |  iGPU Acceleration | dGPU doesn't work |
| ✅     |  Trackpad  | |
| ✅     | Internal Display |   |
| ✅     | HDMI Output | DP won't work as it's connected to the NVIDIA card |
| ✅     | Ethernet |   |
| ✅     | Audio |    |
| ✅     | Battery Status |   |
| ✅     | Lid Detection | Seems sleep doesn't work perfectly  |
| ✅     | Camera / Microphone |  |
| ✅     | Ryzen Power Management | You can use AMD Power Gadget after installing macOS |
| ✅     | Keyboard shortcuts (i.e. Brightness and Volume control fn combos) |  |
| ❌     | NVIDIA GPU | No support for Turing cards |
| ❌     | WIFI & Bluetooth | Realtek WIFI is not compatible with macOS |
| ❕     | USB Tethering | USB Tethering support provided by `HoRNDIS.kext`  |

## Install Notes

- For some reason `NootedRed` doesn't work while installing/updating, please replace `NootedRed` with `WhateverGreen` during installing/updating.
- If you want to use iServices like iCloud, follow [this guide](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#using-gensmbios).
- By default 512MB VRAM is allocated to the iGPU, You're likely to run into issues with that. I recommend you changing it to 4G to avoid instabilities. If you can't change it from the BIOS, you can use [UMAF](https://github.com/DavidS95/Smokeless_UMAF), you should read UMAF instructions carefully before using it.