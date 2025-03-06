---
title: PiHole
description: PiHole Widget Configuration
---

Learn more about [PiHole](https://github.com/pi-hole/pi-hole).

Allowed fields: `["queries", "blocked", "blocked_percent", "gravity", "version"]`.

Note: by default the "blocked" and "blocked_percent" fields are merged e.g. "1,234 (15%)" but explicitly including the "blocked_percent" field will change them to display separately.

Note: the "version" field is off by default but explicitly including the "version" field will cause the widget to make the additional query for version information and display it. The "version" field is only supported for version 6 or higher - it is ignored for version 5 or lower. The "version" field shows the version of the Core component, but if there is a newer version of the Core, FTL, or Web components, then '^' is appended to the version, e.g. "v6.0.5^".

Note: Widget guidelines suggest a max of 4 blocks, so it's not recommended to have both "blocked_percent" and "version" enabled at the same time.

```yaml
widget:
  type: pihole
  url: http://pi.hole.or.ip
  version: 6 # required if running v6 or higher, defaults to 5
  key: yourpiholeapikey # optional, in v6 can be your password or app password
```
