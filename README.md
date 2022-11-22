# MKR1310 Open LoRaWan Modem firwmare update project

This is a packaged version of the [Open LoRaWan Modem](https://github.com/hardwario/lora-modem-abz)
To use it, you just have to run this sketch on arduino and download it to the MKR1310.

**Do this at your own risk, any firmware update can conduct to a break of your board.**

The version of the firmware is 1.2.4 specially patched by the author for MKR1310.

MKR1310 has a different pin setup than the MRK1300 and requires a specific version of the firmware (included here). The next release should include this difference.

# Some of the added features compared to Arduino Original Firmware
- AT+DEVEUI = xxx allows to modify the DEVEUI
- AT$NVM 0,123 / AT$NVM 0 allow to store and read 1 byte into the modem NVM at address [0, 63] address space
- AT$APKACCESS disable the read access to the APPKEY, better to secure the appkey
- AT$DISUART disable the uart, this allows to use the SPI for accessing the onboarded flash

Resume the UART by forcing the LORA_IRQ_DUMB line to LOW
