#PHP MAC Address

This is a PHP class for MAC address manipulation on top of Unix, Linux and Mac
OS X operating systems. it was primarily written to help with spoofing for
wireless security audits.

##Capabilities

  * Verify you are executing it from the command line
  * Verify you are running the script as an administrator
  * Generate new random MAC addresses
  * Validate MAC addresses
  * Get the current system’s MAC address
  * Set or “spoof” any MAC address you want

##Usage

``` php
// require the class
require_once 'php-mac-address.php';

// get the mac address of the eth0 interface
MAC_Address::get_current_mac_address('eth0');

// generate a random mac address
MAC_Address::generate_mac_address();

// validate an MAC address
MAC_Address::validate_mac_address('00-B0-D0-86-BB-F7');

// set a randomly generated MAC address on the eth0 interface
MAC_Address::set_fake_mac_address('eth0');

// set a specific MAC address on the eth0 interface
MAC_Address::set_fake_mac_address('eth0', '00:E4:01:2C:79:DA');
```

For more see the example.php file. You can run the example on the command line
as root. `php example.php`

##Planned Features

  * List all interfaces on the system
  * OS detection
  * Suppress errors on the command line