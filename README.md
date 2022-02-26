# AppleIGB
### Intel onboard LAN driver for macOS. Courtesy of [hnak](https://www.insanelymac.com/forum/profile/228503-hnak/?wr=eyJhcHAiOiJmb3J1bXMiLCJtb2R1bGUiOiJmb3J1bXMtY29tbWVudCIsImlkXzEiOjI3MzA3MywiaWRfMiI6MTc3NTc1Mn0=), refer to the [original post](https://www.insanelymac.com/forum/topic/273073-appleigbkext/) for more details.
<br />

 - Updated to [Intel IGB source v5.7.2](https://www.intel.com/content/www/us/en/download/14098/13663/intel-network-adapter-driver-for-82575-6-82580-i350-and-i210-211-based-gigabit-network-connections-for-linux.html)
 - Adopting/merging IntelMausi link management and code structure approach (for potential further merge)
 - Explicitly stalling packets when transmit queue is busy (as in IntelMausi)
 - Increased default queue capacity from 256 to 1024
 - Added options to (un)select EEE mode (there are notes that disabling it could fix spontaneous link problems)
 - Ensured software interrupt register in watchdog for rx ring cleaned

<hr />

## Supported Devices

 - 82575
 - 82576
 - 82580
 - dh89xxcc
 - i210/i211
 - i350
 - i354

Updated version only tested on AMD versions of Intel I211-AT so far. 

Feel free to post issues (ensure you provide additional device info and whether [SmallTree](https://github.com/khronokernel/SmallTree-I211-AT-patch) is fully working on 11.x)

## Known Current Issues

 - Connection drops. Disconnecting and reconnecting resolves it.
