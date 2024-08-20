### B550M EFI

# Before you download

If you intersted in download this file, please send e-mail to vinicius@sdf.org, so I can provide you the zip password.

# About EFI.zip

This `EFI.zip` file is the first version of my EFI folder, containing the necessary ACPI `.aml files`, `kexts`, `patches`, and a `config.plist` to make macOS 14.6.1 and OpenCore 1.0.1 work with the ASRock B550M Steel Legend motherboard and an AMD Ryzen CPU.

## What's included in this version?

This version includes a `UTBMap.kext` file with all USB ports mapped. This kext works only in conjunction with `USBToolBox.kext`.
I have included three `.aml` files in the `ACPI` folder and an ACPI patch `_PTS to ZPTS` in `config.plist` to fix `Restart/Shutdown/Sleep` problems that I encountered with this motherboard model.
Another patch that I included in the `config.plist` is the AMD Vanilla OpenCore patch for the Ryzen 5700X processor with 8 cores.

## What is working?

- Restart/Shutdown and sleep are working properly.
- DRM and graphics codecs are working properly.
- Audio is working properly.

## What is not working or what I haven't fixed yet?

- Some random errors occur when trying to boot the system, causing a black screen and kernel panic.
- Microphone audio contains noise artifacts.

## List of kexts

- [Lilu.kext](https://github.com/acidanthera/Lilu)
- [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases)
- [WhateverGreen](https://github.com/acidanthera/WhateverGreen/releases)
- [LucyRTL8125Ethernet.kext](https://github.com/Mieze/LucyRTL8125Ethernet)
- [AMDRyzenCPUPowerManagement.kext](https://github.com/trulyspinach/SMCAMDProcessor)
- [SMCAMDProcessor.kext](https://github.com/trulyspinach/SMCAMDProcessor)
- [AppleALC.kext](https://github.com/acidanthera/AppleALC)
- [NVMeFix.kext](https://github.com/acidanthera/NVMeFix)
- [USBToolBox.kext](https://github.com/USBToolBox/tool)
- [UTBMap.kext](https://github.com/USBToolBox/tool)
- [RestrictEvents.kext](https://github.com/acidanthera/RestrictEvents)

## Resources and links

- [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [OpenCore Legacy Patcher](https://dortania.github.io/OpenCore-Legacy-Patcher/)
- [OpenCore bootloader](https://github.com/acidanthera/OpenCorePkg)
- [AMD Vanilla OpenCore](https://github.com/AMD-OSX/AMD_Vanilla)
- [MaciASL](https://github.com/acidanthera/MaciASL)

Last update 08/20/2024
changelog: removed `alcid=11` from `boot-arg` and added `layout-id` in `DeviceProperties`
