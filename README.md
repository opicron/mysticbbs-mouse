# Mouse events in Mystic BBS mods

This Python 2.7 script shows an example how to use mouse events in your mods. 

Currently I tested functionality under Netrunner, Syncterm and fTelnet. Icyterm doesnt have mouse event support yet.

https://github.com/rickparrish/fTelnet/issues/32
https://github.com/mkrueger/icy_tools/issues/112

In Mystic you use `getkey()` and `keypressed()`. Replace these with `getkey_custom()` and `keypressed_custom()`.

## Keypressed()

Returns true or false when chars are in the buffer

## Getkey()

Returns an dict of `[key, extended, mouse]`.

Mouse is a dict of `[x,y,timestamp]`. The timestamp is used to detect double click functionality.

Key is the key pressed. When mouse event is used key is `0,1,2,3` or `4` on doubleclick.

Extended is `true` when an extended key is pressed, `false` otherwise.

