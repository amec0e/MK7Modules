# MK7Modules
Modules which I edited for the WiFi Pineapple MK7.

## DISCLAIMER:

Please keep in mind these are not entirely well crafted. There may also be potential bugs, however they perform the operations for the intended tasks!

Please **use at your own risk!**

Myself (amec0e) assumes NO liability or responsibility for any misuse or unintended consequences resulting from the use of these tools.

These tools are provided with the expectation that users will comply with all applicable laws and regulations. They are intended for educational and research purposes only.

**Please note:** Myself (amec0e) DOES NOT provide support for these tools.

## MDK4E Module:

**Module Author:** newbi3 (Apologies, I could not find a social link!)

I do not want to take any credit away from the original author at all in anyway as they gave me a great base to work with. Here I have edited and added 3 new options to work with the WebUI Interface. -B -E and -S (Single AP BSSID, ESSID and Station BSSID).

**Usage:** Simply remove the old module and reboot your Pineapple before you then sideload the new one from the modules tab in the WebUI.


## MACInfo Module:

**Module Author:** [KoalaV2](https://github.com/KoalaV2)

Again I do not want to take any credit away from the original author, fantastic module. Having said that, I used Prompt Engineering here to re-write the module.py that operates this to allow better searching for full OUIs instead of being limited to just the first 3 octets and using pineapples default OUI list (which is okay but I wanted more).  

This also includes the entire Maclookup.app OUI database to use with this allowing for a much more expanded OUI Macinfo database. The online side of this has also been completely removed as the site it was trying to communicate with was broken when searching and I did not want to fix it when we have a much bigger database now than we did.

**Usage:** Simply remove the old module and reboot your Pineapple before you then sideload the new one from the modules tab in the WebUI.

**To Update the OUI List:**

1. Remove the module from the modules tab in the WebUI as you normally would using the trashcan icon.
2. Using Web Terminal run: `rm -rf /root/.MACInfo/`
3. Reboot Pineapple. **(Important)**
4. Extract the MACInfo directory from within the archive and change into the MACInfo directory.
5. Replace your MLA_OUI_COMPLETE file with your Updated one named exactly the same.
6. Repackage the directory as the extension tar.gz (I used 7z to package as a tar first and then as a gz).
7. Sideload the module and then attempt to search a mac address (or just click search). This will perform the setup and relocation of the MLA_OUI_COMPLETE file to `/root/.MACInfo/`.
