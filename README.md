############################################
# CGminer 4.9.2 GekkoScience Compac BM1384 #
############################################

This is a cgminer 4.9.2 with support fot GekkoScience Compac BM1384 Support.

This software is forked from cgminer 4.9.2 original from ckolivas.

(you can refer to original documentation to docs/README)

## GekkoScience Usb miner ##

![](https://raw.githubusercontent.com/wareck/cgminer-gekko/master/docs/gekko.jpg)

This software use a slighty moddified driver from novak's gekko driver.

I allows working with icarus miner and gekko on same rig.

to build this specific code:

	sudo apt-get update
	sudo apt-get install build-essential autoconf automake libtool pkg-config libcurl4-openssl-dev libudev-dev \
	libjansson-dev libncurses5-dev	libudev-dev libjansson-dev
	./autogen.sh
	./configure --enable-scrypt --enable-lketc
	make

### Option Summary ###

```
  --compac-freq <clock>   Chip clock speed (MHz) default is 150 Mhz
```

## Nicehash extranonce support ##

You can use your miner with last extranonce support for nicehash by adding #xnsub at the address end, like this:

	./cgminer --scrypt -o stratum+tcp://scrypt.eu.nicehash.com:3333#xnsub -u my_btc_address -p x --lketc-clock 280
	