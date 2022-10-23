## Introduction
The following is a document that describes my attempts to implement rtlamr and rtlamr-collect in my home environment.

## Hardware Used
- Raspberry Pi 3B+ (rbpi3b)
- Raspberry Pi 4 (rbpi4)
- Nooelec NESDR Smart V4 (ASIN B01GDN1T4S)

## Software Used
- Ubuntu 22.04.1 LTS (GNU/Linux 5.15.0-1017-raspi aarch64)
- Docker
- rtl-sdr (rtl_tcp)
- rtlamr
- rtlamr-collect
- influxdb

## Work Log
Like a lot of my projects I started out in Windows playing with the capabilities available to me. A few years ago I had purchased a couple of Nooelec SDR's from Amazon, intending to use them for various purposes (recording FM Radio, listening in to open radio traffic, and monitoring our electric meters).

I had ran across the [rtlamr](https://github.com/bemasher/rtlamr) project when I was first getting into SDR's and was super excited to have it setup to monitor the various utility meters around the house. However after getting an initial version up and running, and identifying all of our utility meters back in 2019 I lost interest in getting it to work in an automated fashion.

Fast-forward to October 2022 and we've got our solar system installed, so suddenly I became really interested in watching the consumption on our net meter from Northwestern Energy (NWE), especially with regards to it rolling backwards. While the Solar System (Enphase Envoy) has some of these statistics built into the system, I am most interested in what the meter says, as that is all NWE cares about when it comes to consumption/billing.

This meant that I really needed to work on getting a more automated/always-on solution as opposed to my windows boxes. I have had a couple of Raspberry Pi's laying around that I have used for various projects on and off. They're great little boxes, but not very powerful. I had originally looked to run SoapySDR on the Raspberry Pi 3 which had really fallen to disuse after I received a Raspberry Pi 4 from a brother in law for Christmas in 2021.
