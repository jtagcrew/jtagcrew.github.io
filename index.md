# JTAG Crew (just a bunch of people having fun with JTAG interfaces)

## What is JTAG?

JTAG is a standard originally designed for testing electrical connections between components on a printed circuit board.

While it still serves that purpose, it has evolved to provide debugging capabilities on CPUs, DSPs, FPGAs, etc. For instance you can use JTAG to change a register value on a micro-controller while it is running.

## Why would I want to play with JTAG?

Do you have old gateways from your ISP that aren't worth anything? Using JTAG you could flash a newer firmware like OpenWRT, and you could breathe new life into an obsolete device.

JTAG might be also interesting for reverse engineers. JTAG interface usually expose lots of informations about the internals. That's how Geohot hacked the original iPhone...

## What do I need to play with JTAG?

You will need two things :
 * A hardware interface that will be electrically connected to the board you want to play with
 * A software talking to the hardware interface

### JTAG software ([more...](software.md))

There are multiple JTAG solutions availables. Two of the most common ones are [OpenOCD](http://openocd.org/) and [UrJTAG](http://urjtag.org/).

There is no perfect JTAG software, as each IC has its own JTAG specs (IR length, instruction set, etc.). OpenOCD is what the cool kids use but sometimes it is better to use UrJTAG if you are hacking old Broadcom routers, or if you are thinking about modifying its source code. Sometimes you will have to choice but to use the IC's manufacturer software to interact with the chip.

### JTAG interface

There are many options if you are to get one. Depending on which JTAG software you will be using, you should check for its compatibility.

Commercial JTAG interfaces compatible with proprietary software are generally very expensive (an [XDS510](http://www.spectrumdigital.com/xds510-usb-jtag-emulator/) is over $1000). Open source JTAG software are generally compatible with cheaper JTAG probes: if you are on a tight budget and want to use UrJTAG you can get a frugal but working USB JTAG dongle for less than $2 with [DirtyJTAG](https://github.com/jeanthom/dirtyjtag).
