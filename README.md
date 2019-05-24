## MoonFLTK: Lua bindings for FLTK-1.3.5-2-ts

MoonFLTK is a Lua binding library for the [Fast Light Toolkit (FLTK)](http://www.fltk.org/) and it modified for my [clone](https://github.com/rageworx/fltk-1.3.5-2-ts).

### Requirements
- G++ ( even works on MSYS2 and MingW-W64 )
- [Lua 5.3](http://www.lua.org/) or better
- [FLTK 1.3.5-2-ts](https://github.com/rageworx/fltk-1.3.5-2-ts)

### Original Author
- [Stefano Trettel](https://www.linkedin.com/in/stetre)

### Forked & Modified
- [rageworx](https://github.com/rageworx)

### LUA
[![Lua logo](./doc/powered-by-lua.gif)](http://www.lua.org/)

#### License
- MIT/X11 license (same as Lua). See [LICENSE](./LICENSE).

#### Documentation

See the [Reference Manual](https://stetre.github.io/moonfltk/doc/index.html).

#### Getting and installing

Setup the build environment as described [here](https://github.com/stetre/moonlibs), then:

```sh
$ git clone https://github.com/stetre/moonfltk
$ cd moonfltk
moonfltk$ make
moonfltk$ make install # or 'sudo make install' (Linux)
```

#### Example

```lua
-- Script: hello.lua

fl = require("moonfltk")

win = fl.window(340, 180, arg[0])
box = fl.box(20, 40, 300, 100, "Hello, World!");
box:box('up box')
box:labelfont(fl.BOLD + fl.ITALIC)
box:labelsize(36)
box:labeltype('shadow')
win:done() -- 'end' is a keyword in Lua
win:show(arg[0], arg)

return fl.run()
```

The script can be executed at the shell prompt with the standard Lua interpreter:

```shell
$ lua hello.lua
```

Other examples can be found in the **examples/** directory contained in the release package
(the **examples/fltk** subdirectory contains portings to MoonFLTK of most of the examples
that come with the FLTK distribution).

#### Tested on
	- Linux Mint 18.3, x86.64
	- Embedded Linux
		- Raspberry Pi3B+ ( armhf, debian, lxde )
		- Rock960B ( Rockchip RK3399 - aarch64, debian, lxde )

#### See also

* [MoonLibs - Graphics and Audio Lua Libraries](https://github.com/stetre/moonlibs).

