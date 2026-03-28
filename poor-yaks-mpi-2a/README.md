# "Coco-Extender 2A" a.k.a. "A POOR YAK'S MPI"

NOTA BENE: This is not a consumer-friendly MPI.  It is more of an
experimenter's tool.  PLEASE READ THIS ENTIRE FILE so you will understand
the limitations!

This multi-slot Coco Extender is roughly a simple "Y cable" that brings
all the signals directly from the Coco's edgecard socket to up to five
edgecard slots.

All signals are ganged directly to the same pin number on all sockets,
with these exceptions:

* Pins 1 and 2, reserved for +12V and -12V, are never connected
    to anything.

* The +5V from the Coco is not wired to anything. 
    (Instead, you must provide an external +5VDC supply
    to the small connector in the corner, to power the
    +5V pins on the edgecard sockets.)

* /CTS and /SCS (that is, the active-low enables for Cartrige
    Rom and Floppy Disk controller) are wired to the first
    connector, and not to any others.   The others get +5V
    instead, the inactive voltage for these signals.

There is no buffering on this extender, so you may not be able to use
all the slots, without putting too large a load on your poor little Coco.

The Fifth slot could be used for a fifth edgecard socket, but I like to
solder pin headers on it, and use it as debug signals for an oscilloscope.

The 8-pin header in the lower right corner of the board is where you
must provide +5VDC from an external supply.  That will be the +5V to
all of the edgecard sockets (but not to the Coco itself!).  Here is
an example 3A 5VDC supply that is under $10 on Amazon that comes
with a plug adapter that is easy to wire to the power pin headers:
https://www.amazon.com/MTYTOT-Adapter-100V-240V-Converter-Security/dp/B0BV64MHY6/

This schematic has no surface mount components and needs no assembly by
the PCB maker.  But you'll have to get your own 40-pin edgecard sockets
and your own pin headers, and solder them on.
