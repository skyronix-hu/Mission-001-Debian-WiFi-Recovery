# Mission-001-Debian-WiFi-Recovery
## Goal
Replace an unstable Realtek RTL8723BE Wi-Fi adapter with a TP-Link Archer T2U Plus USB adapter on Debian 13 to restore a stable wireless connection.

## Hardware

- Laptop: ASUS X540LA
- Operating System: Debian 13
- Original Wi-Fi: Realtek RTL8723BE
- New Wi-Fi: TP-Link Archer T2U Plus (RTL8821AU)

## Problem

The built-in Realtek RTL8723BE Wi-Fi adapter was unstable on Debian 13. The connection frequently became unavailable, making the system unreliable for daily use and remote administration.

<img width="774" height="130" alt="01-lsusb" src="https://github.com/user-attachments/assets/dc7d8cdb-c6e2-4f6e-9e1a-17c3dda87416" />

**Figure 1.** Debian 13 successfully detected the TP-Link Archer T2U Plus USB Wi-Fi adapter.

## Solution

The following steps were completed to solve the problem:

1. Verified that Debian detected the USB Wi-Fi adapter.
2. Identified the chipset (RTL8821AU).
3. Installed the required Linux driver.
4. Disabled the unstable internal Realtek RTL8723BE driver.
5. Connected Debian using the TP-Link Archer T2U Plus.
6. Verified a stable wireless connection.

<img width="747" height="117" alt="02-nmcli-device-success" src="https://github.com/user-attachments/assets/aaed4d8a-ee2f-4839-a4fe-b40d613ebbb2" />

<img width="648" height="212" alt="04-ping-test" src="https://github.com/user-attachments/assets/4744cc48-9b08-4a36-b6cd-82f9c65ab1c3" />

<img width="1107" height="134" alt="05-ip-address" src="https://github.com/user-attachments/assets/ef352452-41e1-4119-843e-bd89695209ec" />




## Verification

The solution was verified using the following checks:

- Debian detected the TP-Link Archer T2U Plus USB adapter.
- The new Wi-Fi interface was successfully created.
- The system connected to the wireless network using the USB adapter.
- Internet connectivity was verified.
- The internal Realtek RTL8723BE adapter was disabled.

- ## Lessons Learned

Instead of buying a new laptop, I decided to give my old ASUS X540LA another chance by replacing its unstable Wi-Fi adapter with an inexpensive USB adapter.

This project taught me that systematic troubleshooting is far more effective than guessing or randomly trying commands. I learned how to use Linux tools such as `lsusb`, `dmesg`, `nmcli`, and kernel modules to identify and solve a real hardware compatibility problem.

It also marked my return to Linux after almost twenty years. While working on this project, many memories came back from the Debian Potato and Woody era, reminding me why I enjoyed Linux in the first place.

This repository is the first step in documenting my journey as I build my own Linux and cybersecurity home lab.

