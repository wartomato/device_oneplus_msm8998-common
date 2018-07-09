**A full backup to external sources, a format on the data partition (to EXT4) plus disabling all lockscreen security options (just use "Swipe") is mandatory before updating or you'll see "Error 7" in TWRP.
Since this build, flashing from/to an encrypted ROM or OxygenOS no longer requires the need to format the data partition.**

*Q: Why FBE (File-based Encryption)?*
A: Google decided to use FBE from Nougat onwards and supports it on EXT4. OnePlus decided to do the same on this device. Full Disk Encryption (FDE) is still buggy in TWRP.

*Q: So what are the advantages?*
A: We follow Google and OnePlus on their way to a more secure device and the protection of your data. New users from other encrypted ROMs or stock OOS will no longer need to format the userdata partition.

*Q: But what if I don't want FBE?*
A: Well, it's set to enforcing. You'll get an "Error 7" in TWRP, when you're trying to flash the new version without FBE enabled.
   This means that you do **NOT** have the option be to flash a "no_dmverity.zip" or a similar patch before/after the ROM file...

*Q: How to enable FBE? What do I have to do?*
A: You do not have to do anything on an already encrypted device. From an unencrypted device, please backup all your data (including internal storage!!!) via TWRP and copy it to an external source.
   Afterwards format your data partition **twice**, then just flash the ROM.

*Q: What happens, if I don't follow the instructions, e.g. getting the "Error 7"?*
A: Running a FBE-enabled ROM on a FBE-disabled phone will cause boot loops. So a check for FBE was implemented that prevents you from flashing "by accident" on an unencrypted device.
