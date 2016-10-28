BP Tracker Firmware
==========

Provides a particle.io [cloud API][cloudapi] to monitor the device and receive alerts when the core moves away from a dynamic geofence.

[![Build Unstable][shield-unstable]](#)
[![MIT licensed][shield-license]](#)



Table Of Contents
-----------------

- [Requirements](#requirements)
- [Usage](#usage)
- [Cloud API](#cloud-api)
- [Additional Resources](#additional-resources)
- [License](#license)

Requirements
-------
BP Tracker requires the following:

  * particle.io [electron][electron] core (tested with 0.5.3 firmmware)
  * [AssetTracker][assetrackershield] shield (tested with v002)
  * [particle cli][particlecli]

Usage
-----

The firmware can be flashed on the hardware using the particle cli:

```sh
particle compile electron ./electron
particle flash --serial firmware_electron_xxxxxxxxxxxxx.bin
```

Then you can make queries on the API to configure and interrogate the device.
For example:

```
// get the GPS coordinates in a bpt:gps event
curl https://api.particle.io/v1/devices/<device_name>/bpt:gps -d access_token=<token>

```

TODO

Cloud API
-----

BP tracker utilizes particle.io's cloud service to interface with client applications. The table below summaries all the functions
that can be called on the device. <wip>


Additional Resources
-----

...


License
-------

BP Tracker Firmware is licensed under the [MIT][info-license] license.  
Copyright &copy; 2016 Derek Benda


[shield-unstable]: https://img.shields.io/badge/build-unstable-red.svg
[shield-license]: https://img.shields.io/badge/license-MIT-blue.svg

[particlecli]:https://docs.particle.io/guide/getting-started/connect/electron/
[particleio]: https://www.particle.io/
[electron]: https://www.particle.io/products/hardware/electron-cellular-dev-kit
[cloudapi]: https://docs.particle.io/reference/api/
[assetrackershield]: https://docs.particle.io/datasheets/particle-shields/#electron-asset-tracker
[info-license]: LICENSE
