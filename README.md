# iso2disk

This script is a command-line helper for burning an iso file to any specific device,
on Apple OS X.

I wrote the script when I got disgusted how awkwardly complicated it is on OS X to
write a simple iso file to an USB stick.

## It comes handy when:

- you want to burn a CD or DVD from an ISO file
- you want to create a boot disk for Windows or any *nix operation systems

## How to use

- iso2disk help - shows you the supported functions
- iso2disk devices - creates a list of currently active devices
- iso2disk convert <output> <input> - this function converts an iso to an img file *2
- iso2disk burn <img/path> - this will burn the content of the img file to a later specified disk (prompt)
- iso2disk all <output> <input> - this is the shorthand for convert and burn together

Download the file, give it the right permission and run it like this:

	bash$ ./iso2disk convert ubuntu.img ubuntu.iso
	Converting ubuntu.iso to ubuntu.img ...
	Conversion done ...
	bash$

Then:

	bash$ ./iso2disk burn ubuntu.img
	1. /dev/disk0
	2. /dev/disk0s1
	3. /dev/disk0s2
	4. /dev/disk1
	Please select a device. [1-       4]: 4<enter>
	Burning...

This does the job. I selected 4 in the example, because that is the USB stick, I wanted copy the iso to.
	