# avahi-tools-docker
Simple Alpine-based Docker image containing the avahi-tools package.

Allows the publication of mDNS services from a Docker container if the host is running an instance of Avahi already.

Especially useful on, for example, a Synology NAS which already is running Avahi as part of its base system.

Usage:
```
docker run -v /run/dbus:/var/run/dbus -v /run/avahi-daemon:/var/run/avahi-daemon --network host petercv/avahi-tools:latest avahi-publish -s <service> _ipp._tcp 631
```
