# ME cleaner

A cleaner for Intel ME images.

This tools removes any unnecessary partition from an Intel ME firmware, reducing
its size and its ability to interact with the system.
It should work both with Coreboot and with the factory BIOS.

Currently this tool:
 * Scans the FPT (partition table) and checks that everything is correct
 * Removes any partition entry (except for FTPR) from FPT
 * Removes any partition except for the fundamental one (FTPR)
 * Corrects the FPT checksum

Current status:

| Architecture  | Status		|
|---------------|-----------------------|
| Nehalem	| DOESN'T WORK (yet)	|
| Sandy Bridge	| WORKS			|
| Ivy Bridge	| WORKS			|
| Haswell	| UNTESTED		|
| Broadwell	| UNTESTED		|
| Skylake	| SHOULD WORK		|

Special thanks to Federico Amedeo Izzo for his help during the study of Intel
ME.

