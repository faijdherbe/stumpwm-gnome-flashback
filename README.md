# stumpwm-gnome-flashback [![LICENSE](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](http://choosealicense.com/licenses/mit/)

Allows you to use stumpwm in a GNOME-Flashback session. Large parts of this are based on the existing [`i3-gnome`](https://github.com/lvillani/i3-gnome) and [`i3-gnome-flashback`](https://github.com/regolith-linux/i3-gnome-flashback) projects.

This has been tested working on GNOME version **40**.

# Installation

For Ubuntu (19.10), ensure prerequisites are installed:

```
sudo apt install stumpwm gnome-flashback build-essential
```

Then install stumpwm-gnome-flashback:

```
sudo make install
```

For other distributions, clone this repository and run `make install` with root privileges.

# Notes

To understand how the files in this repo work to initialize an stumpwm and GNOME session, refer to this [GNOME wiki](https://wiki.gnome.org/Projects/SessionManagement/RequiredComponents) on session management.

The default session for `stumpwm-GNOME-Flashback` installs a set of configuration defaults for GSettings/dconf, e.g.:

  - Desktop icon handling is disabled for GNOME Flashback, due to incompatibilities with stumpwm, and control of the root window is instead given to `gnome-control-center`, which handles setting the user-defined wallpaper, among other things.

  - Window buttons for minimize and maximize have been removed, leaving only the close button, as the former are ineffectual in stumpwm.

Setup for these configuration defaults is handled via GSettings overrides, which are described in
further detail
[here](https://help.gnome.org/admin/system-admin-guide/stable/dconf-custom-defaults.html.en) and
[here](https://help.gnome.org/admin/system-admin-guide/stable/overrides.html.en).
