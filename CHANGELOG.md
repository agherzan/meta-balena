Change log
-----------

* meta-resin switched to systemd now instead of sysvinit [Theodor]
* Forcefully remove supervisor container to avoid some issues where a normal remove won't work even though the container is stopped [Page]

# 2015-05-20

* Stop spawning getty in production builds [Theodor]
* Add iozone to staging build [Theodor]
* Add support for unprotected WiFi Tethering with Connman [Praneeth]
* Add support for Adafruit Touch Screen - Switches to using adafruits fork of fbtft [Praneeth]
* Add support for Parallella [Theodor]

# 2015-05-07

* Fix beaglebone connman not starting [Praneeth]

# 2015-05-05

* Fix the DNS bug occurring because of docker/rce copying resolv.conf before network connectivity. [Praneeth]
* Change Staging API url to api.staging.resin.io from staging.resin.io [Praneeth]

# 2015-04-27

* Fix resin-net-config to honour network.config and ethernet.config as per the changes in resin-image-maker. [Praneeth]
* Add tun to NetworkInterfaceBlacklist of connman. [Praneeth]
* Add --nodnsproxy to connmand startup in both systemd services and init scripts, This disables the internal dns proxy of connman. [Praneeth]
* Wait for docker to terminate before calling unmount in resin-supervisor-disk [Praneeth]

# 2015-04-19

* Allowed concurrent building on the resin-supervisor recipe.
* Fixed first boot connectivity.
* Added a script to balance the btrfs partition on boot and every 24 hours at midnight
