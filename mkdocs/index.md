Binary Data Stream

Overview
================================================================================

**TODO**

Quickstart
================================================================================

 1. Install wish with pip ([instructions](installation)).

 
------


Most of the features of bitstream are available via the `BitStream` class.

    >>> from bitstream import BitStream

The module is tightly integrated with the [NumPy][NumPy] library. 
For convenience, we import all symbols from its top-level module.

    >>> from numpy import *



Overview of Bitstream Features
================================================================================ 

    >>> stream = BitStream()
    >>> stream
    <BLANKLINE>
    >>> stream.write(True, bool)
    >>> stream
    1
    >>> stream.write(False, bool)
    >>> stream
    10
    >>> stream.write(-128, int8)
    >>> stream
    1010000000
    >>> stream.write("AB", str)
    >>> stream
    10100000000100000101000010
    >>> stream.read(bool, 2)
    [True, False]
    >>> stream
    100000000100000101000010
    >>> stream.read(int8, 1)
    array([-128], dtype=int8)
    >>> stream
    0100000101000010
    >>> stream.read(str, 2)
    'AB'
    >>> stream
    <BLANKLINE>

