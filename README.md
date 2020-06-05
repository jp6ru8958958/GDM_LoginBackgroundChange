# GDM_LoginBackgroundChange
### A correct way to change gdm login screen's background into user's image.

```
sh extractgst.sh
```
```
cd shell-theme/theme
```
```
vim gnome-shell-theme.gresource.xml
```
```
gnome-shell-theme.gresource.xml
```
```
<?xml version="1.0" encoding="UTF-8"?>
<gresources>
  <gresource prefix="/org/gnome/shell/theme">
    <file>calendar-today.svg</file>
    <file>checkbox-focused.svg</file>
    <file>checkbox-off-focused.svg</file>
    <file>checkbox-off.svg</file>
    <file>checkbox.svg</file>
    <file>dash-placeholder.svg</file>
    <file>gnome-shell.css</file>
    <file>gnome-shell-high-contrast.css</file>
    <file>icons/message-indicator-symbolic.svg</file>
    <file>key-enter.svg</file>
    <file>key-hide.svg</file>
    <file>key-layout.svg</file>
    <file>key-shift-latched-uppercase.svg</file>
    <file>key-shift.svg</file>
    <file>key-shift-uppercase.svg</file>
    <file>noise-texture.png</file>
    <file>LoginBackground.png</file>
    <file>no-events.svg</file>
    <file>no-notifications.svg</file>
    <file>pad-osd.css</file>
    <file>process-working.svg</file>
    <file>toggle-off-hc.svg</file>
    <file>toggle-off-intl.svg</file>
    <file>toggle-on-hc.svg</file>
    <file>toggle-on-intl.svg</file>
  </gresource>
</gresources>
```
```
$ vim gnome-shell.css
```
> (Find and edit #lockDialogGroup like below and edit background-size):
```
#lockDialogGroup {
  background: #2e3436 url(LoginBackground.png);
  background-size: 1600px 900px;
  background-repeat: no-repeat;
}
```
```
$ glib-compile-resources gnome-shell-theme.gresource.xml
```
```
$ sudo cp gnome-shell-theme.gresource /usr/share/gnome-shell
```
```
$ reboot
```
