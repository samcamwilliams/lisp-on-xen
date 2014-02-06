lisp-on-xen
===========

A port of Kernighan &amp; Ritchie's 1988 LISP interpretation to barebones Xen (as a stub domain).

This is a very rough implementation, it is clearly not fit for production use! Despite this, it may serve as a reasonable example of how to implement small stub domains.

## Usage ##

* Move everything into the `stubdom` directory of a Xen source tree. (Note: this will destroy anything you may already have in your `c` stubdom!)
* Optionally, apply `no-printk.patch` in `extras/mini-os/console/`. This will remove a lot of (unnecessary and ugly) console output at startup. Be aware that this will affect (and possibly break) other stubdoms.
* Run `make c-stubdom` from the `stubdom` directory.
* Create a new DomU with `mini-os-x86_64-c/domain_config`.
* Have fun! Double tap escape to shutdown the instance.

## Future Work ##

None planned, this is only intended to be a demo.

## Known Issues ##

* If you are using a processor arch that is not x86\_64, you will need to change the name of the `mini-os-x86_64-c` directory accordingly.
