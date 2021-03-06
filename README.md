# wrenjs
Using [emscripten](https://emscripten.org/)
to transpile Bob Nystrom's [wren](http:wren.io) programming language to Javascript.

wren: 0.3.0 | emscripten: 2.0.10

### Quick Start

There should be a prebuilt copy of the library in the `out` directory, that
you can just add to your html document.

    <script src="js/wren.min.js"></script>

After that, you'll be able to access and use the `Wren` object to create a VM.

    // Give this a shot, and take a peek in the console.
    let vm = new Wren.VM();
    vm.interpret('main', 'System.print(123456)')


For the most part, all the wren C api functions are implemented as methods on
the Wren.VM.

For Example:
`wrenSetSlotString(vm, slot, string)` becomes `vm.setSlotString(slot, string)`

### Documentation

Documentation is a little sparse at the moment.

[Configuring the VM](./docs/configuration.md)

### Build Instructions

These instructions are for an Ubuntu-like system.

You will need:
- build-essential
- cmake
- python2.7
- nodejs
- java

After these are installed, run `./build.sh`

For a detailed explanation of what this bash script does,
feel free to check out the comments in the file itself.
