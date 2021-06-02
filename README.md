Raspberry PI Bootstrap
=========

Ansible role for Raspberry PI Bootstrap with bare essentials features

Functionality
-------------

Role deploys some bare essentials settings and apps for any Raspberry Pi installation.
In the future, is possible to deploy multiple apps and settings.
The basic config for Raspberry Pi hardware settings are done using *raspi-config* default utility.


For populating the Ansible facts with Raspberry Pi capabilities is used on pre-init task the same default utility *raspi-config*

In this role enables:
* i2c RTC clock for *ds1307|pcf8523|ds3231*
* I2C/SPI serial shield that is using *SC16IS752*
* [Telegraph](https://www.influxdata.com/time-series-platform/telegraf/) server for sending graphs data to a specified server
* [Cloudflare](https://api.cloudflare.com/) Dynamic DNS client
* [Monitorix](https://www.monitorix.org/)


Dependencies
------------

No dependencies are used and are needed to use this role

Example Playbook
----------------

You can include the role in any playbook that is used on Raspberry pi deploy

    - hosts: servers
      roles:
         - { role: rpi_bootstrap }

### 🌍 Contributions

Contributions of all forms are welcome :)

## 🗒 License

This Ansible role is licensed under the GNU General Public License, version 3 (GPLv3).

## 👀 Author

**Zaharia Constantin**

[View my GitHub profile 💡](https://github.com/soulraven)
