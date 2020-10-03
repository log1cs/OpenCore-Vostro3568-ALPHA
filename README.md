***** UPDATE: I DON'T USE VOSTRO 3568 ANYMORE SINCE I WAS CHANGED TO XPS 13 2020. I STILL UPDATE THE EFI EVERYDAY WHEN IT COME STABLE. *****


OpenCore 0.6.1 for Vostro 3568.

This is a OpenCore-based EFI for Dell Vostro 3568. REMEMBER: THIS IS THE ALPHA VERSION. YOU MIGHT FACE BUG WHILE USING.

I'm using a Vostro 3568 i3 version.

About the specs:
 
 + CPU: Intel Core i3-7020u 2.3GHz
 + RAM: 4GB DDR4 2133Mhz
 + SSD: 240GB HP S400 SATA3 SSD
 + Display 1366x768
 + Audio: Realtek ALC256 Audio Controller
 + Intel Dual Band AC-3165
 + Realtek RTL8111

 + Since I hasn't fix the graphics yet. You need to use OpenCore with my Clover framebuffer patch or the patch I'm following on Dortania OpenCore Guide.




| Feature | Status | Notes |
| ------------- | ------------- | ------------- |
| **Intel iGPU** | Testing | Testing, will be updated soon |
| **Trackpad I2C ** |  ✅ Working | Full gesture support. Probably the not-actually touchpad experience on a non-mac. | 
| **iMessages and App Store** | ✅ Working | Just follow the OpenCore Guide (#ℹ️-changing-serial-number,-board-serial-number-and-smuuid) |
| **Speakers and Headphones** | ✅ Working | To permanently fix headphones follow this link below |
| **Built-in Microphone** | ✅ Working |
| **Webcam** | ✅ Working | Fully working, is detected as Integrated Webcam |
| **Handoff** | ✅ Working |
| **Wi-Fi/BT** | ✅ Working | The stock AC3165 Wi-Fi card is working perfectly fine. But I recommend |
| **Fingerprint reader** | ❌ Not working | Probably will never work, because proprietary Synaptics drivers that only exist for Windows are needed. Will patch to disable it. |
| **SD Reader** | ❌ Not working | The USB2.0 SDCard Reader from Realtek never working on Mac because drivers is only for Windows. Will patch to disable it. |




FOR AUDIO FIXING USE THIS GITHUB REPO AND FOLLOW THE INSTRUCTIONS: 
https://github.com/hackintosh-stuff/ComboJack


+ Guide :

1. Delete CodecCommander.kext，put ComboJack_Installer/VerbStub.kext in Clover/kexts/Other
2. Run ComboJack_Installer/install.sh in terminal and reboot
3. Done. When you attach a headphone there will be a popup asking about headphone type.
