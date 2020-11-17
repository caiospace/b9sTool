#### Instructions

https://3ds.hacks.guide/<br>
- WARNING: Never, under any circumstance, use this homebrew in conjunction with a youtube/video guide of any kind!<br>

#### General Info

- This app only writes to FIRM0, not FIRM1, so it should be safe given your FIRM1 is not corrupt or a9lh'd.<br>
- Never use this on anything but 3DS FIRM 11.14.0-YZ<br>
- Never use this if sighax/b9s is already installed (on any firmware)! The result will be a sloppy uninstallation at best and a brick at worst<br>
- Be cautious when using this with arm9loaderhax installed, as the special handling for it is still experimental

Compiling: 
- Just supply the current decrypted FIRMs for both new/old 3ds and put them in the firm_new and firm_old 
directories respectively. Then place the newest boot9strap.firm payload in the payload directory. You will also
need to supply a clean secret_sector.bin in the a9lh_files/secret_sector directory if you want the arm9loaderhax
handling to work on n3ds systems without a the user supplying that file. Then compile with
make FIRM_INFO="11.10 only" or whatever is actually the firmware range of the current native firm.
The user does not have to supply any extra files like in previous versions. Needs the latest libfat version.

### Important b9sTool 5.X.X differences to 4.X.X

BACKUP.bin:<br>
- This has been removed. This feature was made in the interest of safety, but the realization that the update trick can reliably restore corrupted firms made it redundant.<br>
It was also a pain in the ass.<br><br>

xorpad_0123ABCD.bin<br>
- This is dumped to your boot9strap folder when b9s is installed. It isn't used now but may be useful in the future. Don't delete it.<br>
The hex number in the filename is the first 4 bytes of the file's SHA1.<br><br>

Cycling firm types:<br>
- When you install boot9strap multiple times, the standard behavior is that it will cycle between b9s and stock firm.<br>
Don't count on this though, it's just a property of xoring operations and really isn't intended.<br>
It is recommended you only install boot9strap once.<br><br>

Firmware info:<br>
- 6.0.1 is for firmware 11.14 ONLY (always check the firmware in the app menu to be sure as this can change as new firmwares are released!)<br>
- 5.0.2 - 6.0.0 is for firmware 11.13<br>
- 4.0.1 - 5.0.1 is for firmwares 11.8 to 11.10 or 11.11(eur) ONLY<br>
- 4.0.0 is for firmwares 11.4 to 11.7 ONLY<br>
- Be careful using b9sTool between firmware updates -  only use b9sTool on the firmware it's intended for.<br>

#### Credits

+ zoogie, aspargas2, plailect
