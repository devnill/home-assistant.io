---
layout: component
title: "OpenWRT (luci)"
description: "Instructions how to integrate OpenWRT routers into Home Assistant."
date: 2015-03-23 19:59
sidebar: true
comments: false
sharing: true
footer: true
logo: openwrt.png
ha_category: Presence Detection
---

_This is one of the two ways we support OpenWRT. If you encounter problems, try [ubus](/components/device_tracker.ubus/)._

This is a presence detection scanner for OpenWRT using [luci](http://wiki.openwrt.org/doc/techref/luci).

Before this scanner can be used you have to install the luci RPC package on OpenWRT:

```bash
opkg install luci-mod-rpc
```

```yaml
# Example configuration.yaml entry
device_tracker:
  platform: luci
  host: ROUTER_IP_ADDRESS
  username: YOUR_ADMIN_USERNAME
  password: YOUR_ADMIN_PASSWORD
```

Configuration variables:

- **host** (*Required*): The IP address of your router, e.g. 192.168.1.1.
- **username** (*Required*): The username of an user with administrative privileges, usually *admin*.
- **password** (*Required*): The password for your given admin account.

See the [device tracker component page](/components/device_tracker/) for instructions how to configure the people to be tracked.
