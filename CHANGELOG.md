# Changelog

## Unreleased

- Order the Magic Mouse udev rule before systemd seat ACL processing.
- Enable the service under `default.target` so it autostarts on compositors
  that never activate `graphical-session.target` (e.g. labwc).
- Fix ydotoold socket bind failure: `ProtectHome=true` hid `/run/user`;
  services now use `ProtectHome=tmpfs` with `BindPaths=%t`.
- Trigger Back/Forward with a quick one-finger horizontal flick; two fingers
  are now pinch-only by default (`MIN_FINGERS`/`MAX_FINGERS` restore the old
  behavior).

## 0.1.0 - 2026-08-12

- Preserve kernel-native pointer movement and physical buttons.
- Add one-finger high-resolution scroll with sticky axis locking.
- Add mutually exclusive two-finger Back/Forward and native Wayland pinch.
- Add native three-finger GNOME workspace and overview gestures.
- Enable kernel-native center-zone middle click.
- Add isolated uinput capability boundaries and regression tests.
- Add transactional installation, least-privilege udev rules, safe uninstall,
  service hardening, and explicit upstream provenance.
- Tolerate delayed boot-time uinput ACLs without traceback or service restart.
