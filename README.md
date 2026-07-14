# Flydigi-Vader-5S | 飞智黑武士 5S

Fix Flydigi-Vader-5S not working on Linux.

1. `sudo cp 99-flydigi-vader-5s.rules /etc/udev/rules.d/`.
2. `reboot`.
3. Plug and unplug the game controller, it should work.

This [udev] rule doesn't always work. You can manually run the following after each connection.

1. Press the Xbox button (the controller should vibrate and the LED ring change color).
2. Run `sudo bash -c "modprobe -r xpad; modprobe xpad; echo '37d7 2801' > /sys/bus/usb/drivers/xpad/new_id"`.
3. The white LED under the Xbox button should light up, and it should work.

You can also set a shell alias: `alias fv5s="sudo bash -c 'modprobe -r xpad; modprobe xpad; echo 37d7 2801 > /sys/bus/usb/drivers/xpad/new_id'"`.

-----

# 飞智黑武士 5S

修复飞智黑武士 5S 在 Linux 上无法使用。

1. `sudo cp 99-flydigi-vader-5s.rules /etc/udev/rules.d/`。
2. `reboot`。
3. 插拔游戏手柄，应该就能正常使用了。

这份 [udev] 规则并不总是能生效，你还可以在每次连接后手动操作。

1. 按下 XBOX 徽标键 (此时手柄应该会震动，氛围灯改变颜色)。
2. 执行 `sudo bash -c "modprobe -r xpad; modprobe xpad; echo '37d7 2801' > /sys/bus/usb/drivers/xpad/new_id"`。
3. 此时 XBOX 徽标键下方的白色指示灯会亮起，应该能正常使用了。

你也可以设置一个 Shell alias: `alias hws5s="sudo bash -c 'modprobe -r xpad; modprobe xpad; echo 37d7 2801 > /sys/bus/usb/drivers/xpad/new_id'"`。

[udev]: https://en.wikipedia.org/wiki/udev
