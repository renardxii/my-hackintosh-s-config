# my-hackintosh-s-config
my hackintosh's config.plist :D

MLB, SerialNumber, and SystemUUID are replaced by the "null" strings
ROM is replaced by a bunch of zeroes
Replace them accordingly to the OpenCore guide: https://dortania.github.io/OpenCore-Install-Guide/config.plist/haswell.html#platforminfo

# system specs:

Motherboard: FUJITSU D3230-A1

CPU: i5-4440

GPU: GeForce GT 630 2GB (GK107)

RAM: 10GB DDR3 (1600 MHz)

HDD: Western Digital 320 GB

Ethernet: Realtek RTL8111/8168/8211/8411

Audio: Realtek ALC671 (alcid=15)

SMBIOS: iMac15,1

macOS: Sonoma 14.7 if I remember right (but I know it's Sonoma)

If anyone has a similar system or just for the sake of archiving my config.plist in case things ever go south, I uploaded this. I barely use my hackintosh now though.

# kexts, drivers, resources, tools, ACPI and other files needed:
Kexts: AppleALC.kext; Lilu.kext; RealtekRTL8111.kext; SMCProcessor.kext; SMCSuperIO.kext; VirtualSMC.kext; WhateverGreen.kext;

Drivers: HfsPlus.efi; OpenRuntime.efi; ResetNvramEntry.efi;

Resources: [blank], OpenCore should already give you an already-made folder by default, do not edit it unless you know what you're doing.

Tools: OpenShell.efi;

ACPI: SSDT-EC.aml; SSDT-PLUG.aml; (you should use your own ACPI, that's why I'm not sharing mine). I generated mine by using https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-easy.html

Other file necessary is OpenCore.efi (place it at the root of your OC folder)

BOOT has BOOTx64.efi

# what works:
Audio

GPU acceleration (GPU patched with OCLP)

Ethernet

USB ports (no USB mapping was needed)

Most things work decently

# what doesn't work:
microphone

sometimes macOS glitches (but it's expected)

# !! FIRST, ENSURE YOU HAVE iMac19,1 AS YOUR SMBIOS (WHICH REQUIRES DIFFERENT SERIALNUMBER, MLB, ETC.) THEN AFTER YOU INSTALL macOS YOU SHOULD CHANGE IT BACK TO iMac15,1 !! enable -no-compat-check in boot-args before switching your SMBIOS again.
