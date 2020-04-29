This futurerestore build is patched for the restore of custom iPSW on 64bit devices.
Img4tool SHSH build identity checks are disabled, so it's possible to fakesign the iPSW using a shsh ticket for another iOS Version
(for example: I fakesign my iOS 11.4.1 tethered custom iPSW using an APTicket/SHSH for iOS 12.4.6)

To use it, set your device into pwnedDFU, load patched iBSS and iBEC using iRecovery and find out APNonce using igetnonce...
Fetch a new APTicket using tsschecker for latest iOS Version with the nonce you grabbed with igetnonce.
Run futurerestore and enjoy!

# futurerestore
_futurerestore is a hacked up idevicerestore wrapper, which allows manually specifying SEP and Baseband for restoring._

__Only use if you are sure what you're doing.__
---
Latest release available [here](https://github.com/j4nf4b3l/futurerestore/releases) for macOS.

## Features
* Supports the following downgrade methods:
  * Prometheus 64-bit devices (generator and ApNonce collision mode);
  * Odysseus for 32-bit devices;
  * Re-restoring 32-bit devices to iOS 9 with [alitek123](https://github.com/alitek12) no-ApNonce method (alternative — [idevicererestore](https://github.com/s0uthwest/idevicererestore)).
* Allows restoring any non-matching signed iOS/SEP/Baseband.

__NOT recommended to use '-u' parameter, if you update jailbroken firmware!__
# Dependencies
* ## Runtime
  * On macOS, futurerestore requires no runtime dependencies, the following are only for compiling;
  * On Linux, [usbmuxd](https://github.com/libimobiledevice/usbmuxd) is required at runtime;

* ## External Libs
  Required:
  * [libzip](https://github.com/nih-at/libzip);
  * [libfragmentzip](https://github.com/s0uthwest/libfragmentzip);
  * [libplist](https://github.com/libimobiledevice/libplist);
  * [libirecovery](https://github.com/s0uthwest/libirecovery);
  * [libimobiledevice](https://github.com/s0uthwest/libimobiledevice);
  
  Optional:
  * [libipatcher](https://github.com/s0uthwest/libipatcher);

* ## Submodules
  Make sure these projects compile on your system (install their dependencies)
  * [jssy](https://github.com/tihmstar/jssy);
  * [tsschecker](https://github.com/s0uthwest/tsschecker);
  * [img4tool](https://github.com/s0uthwest/img4tool);
  * [idevicerestore](https://github.com/s0uthwest/idevicerestore)
  
## Report an issue
You can do it [here](https://github.com/j4nf4b3l/futurerestore/issues).

## Credits
Creator of [original project](https://github.com/tihmstar/futurerestore) - [tihmstar](https://github.com/tihmstar).
S0uthwest for his precompiled futurerestore build I've patched...


ReadMe updated on:

        2019-07-02
