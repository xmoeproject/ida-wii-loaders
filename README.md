# REL & DOL Loader plugins for IDA Pro

The REL and DOL files are found in Nintendo Gamecube/Wii games. This repository is focused on loading the REL files.

## Environment
* Visual C++ 2010 Express
* IDA Pro 6.1 SDK

## DOL Loader
A fork of the DOL loader by Stefan Esser, source from [here](http://hitmen.c02.at/html/gc_tools.html).

### Changes
* Currently none (will consider bug fixes)

## REL Loader
A rewrite/fork of the RSO loader by Stephen Simpson, source from [here](https://github.com/Megazig/rso_ida_loader).

### Features
* Creates segments/sections (.text, .data, .bss).
* Strips loader data from the binary.
* Identifies functions (prolog, epilog, unresolved).
* Treats relocations to external modules as imported functions.
* Reads module names from external file `module_id.txt` placed in the same folder as the database.
    * In the format `XX name` on each line where XX is a hexadecimal code indicating the module ID and name is the name of the module.


### Planned (TODOs)
* Place header information at the top.
* Treat prolog, epilog, and unresolved as exports.
* Read exported `.map` files to give meaningful names to externals.
* Make imports appear in the imports tab.
* Set compiler options.
* Allow some settings such as relocating to any base.
