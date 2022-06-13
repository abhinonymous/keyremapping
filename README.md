swapping ctrl and alt to make function similar to mac:

https://superuser.com/questions/1190329/can-i-switch-the-alt-and-ctrl-keys-on-my-keyboard
https://www.experts-exchange.com/articles/2155/Keyboard-Remapping-CAPSLOCK-to-Ctrl-and-Beyond.html
https://superuser.com/questions/1131889/disable-all-keyboard-shortcuts-in-windows/1132401#1132401

"Copying relevant info from link above"

You can do it using the registry. Just use one of these two files. First the file for switching the Ctrl Key to Alt and the other switches Left ctrl with caps.

switch_alt_and_ctrl.reg

switch_caps_to_Lctrl.reg

This adds the necessary key to the registry.

After double clicking the reg-file you need to restart/logout-login and you're good.






"Scancode Map" key is a hex-value with the following meaning:
```
00,00,00,00 Header: Version. Set to all zeroes.
00,00,00,00 Header: Flags. Set to all zeroes.
05,00,00,00 5 entries in the map (including null entry).
38,00,1d,00 Left CTRL -> Left ALT (can also be another key).
1d,00,38,00 Left ALT -> Left CTRL.
38,e0,1d,e0 Right CTRL -> Right ALT.
1d,e0,38,e0 Right ALT -> Right CTRL.
00,00,00,00 Null entry.
```


Other useful keys to know:
```
1d 00    Left Ctrl
1d e0    Right Ctrl
38 00    Left Alt
38 e0    Right Alt
5b e0    Left Windows Key
5c e0    Right Windows Key
5d e0    Windows Menu Key
3a 00    Caps Lock
```

