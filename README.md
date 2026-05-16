# OnePlus3-Kali-Nethunter
Everything needed to root and install Nethunter on the OnePlus 3.

I am assuming you know what you are doing. Don't submit an issue because I don't give a shit. I didn't create any of this software I just figured out how to install Nethunter on the OnePlus 3.

You willl need fastboot and ADB.

STEPS:
1. Enable USB debugging. Run [adb reboot fastboot] || Hold down volume down while phone boots.
2. $ fastboot oem unlock
3. $ fastboot reboot
4. Go back to fastboot
5. $ fastboot flash recovery recovery.img
6. The Lineage OS recovery image is now installed. Reboot into recovery.
7. In recovery menu:
     Factory Reset > Format Data/Factory Reset
8. Back to main recovery menu > Apply Update > Apply from ADB
9. $ adb -d sideload path/to/lineageos/zip
  Normally, adb reports Total xfer: 1.00x, but in some cases, even if the process succeeds, the output may stop at 47% and show adb: failed to read command: Success. In other instances, it might display adb: failed to read command: No error or adb: failed to read command: Undefined error: 0 which is also fine.
10. Reboot and set up the phone again. Enable USB debugging and all that.
11. Install Magisk.
12. Go back to fastboot.
13. $ fastboot flash boot [patched boot image] 
14. Now when you reboot, Magisk should be installed.
15. $ adb push path/to/kali/zip /sdcard
16. In Magisk, tap Install > Modules > Install From Storage > Kali ZIP file.
17. Magisk will install the Kali module, after which you can reboot.
18. Repeat steps 15 and 16 for the SpiderBlood kernel.
19. You can now reboot into your Kali Nethunter system.
