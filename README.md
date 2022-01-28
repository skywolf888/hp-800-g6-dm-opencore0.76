# OpenCore EFI for HP EliteDesk 800 g6(macOS 11.6)
## Just for backup

## Specification
| **Component** | **Model** |
| ------------- | --------- |
| CPU | Intel i5-10500T |
| RAM | 1 * 16GB DDR4-2666 |
| Audio Chipset | ALC222 |
| GPU | Intel® UHD Graphics 630 (DP) |
| OS Disk (NVMe) | SN732 NVMe 256G |
| Ethernet | Intel I219-V |

**macOS version**: 11.6
**OpenCore version**: 0.7.6

## How to use

1. Make your USB installer with [**this guide**](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
2. Clone the repository and paste "BOOT" and "OC" directories into your's pendrive "EFI" folder
3. Download [**GenSMBIOS**](https://github.com/corpnewt/GenSMBIOS) to generate unique SMBIOS information. Run it and select **Generate SMBIOS**, as the model select **iMac20,1**.
4. Open config.plist with [**ProperTree**](https://github.com/corpnewt/ProperTree) and go to PlatformInfo > Generic. Set MLB (Board Serial), SystemSerialNumber (Serial) and SystemUUID (SmUUID) to generated values. Change ROM to your network card's MAC address without the `:` character. [**How to get MAC Address?**](https://www.wikihow.com/Find-the-MAC-Address-of-Your-Computer)
5. Boot it!
6. Don't use front right Usb port!

## All work

- CPU
- Dual monitors (two Displayport)
- Audio
- Ethernet
- USB
- Wifi
- App store, iCloud, iMessage, iTunes, FaceTime, etc
- Sleep, Wakeup, Shutdown, Restart

## HIDPI fix

```bash
git clone https://github.com/xzhih/one-key-hidpi.git
cd one-key-hidpi
./hidpi.command
```
