# pysodium-cardano

[Pysodium](https://github.com/stef/pysodium) is a very simple wrapper around the 
[libsodium](https://doc.libsodium.org/) cryptographic library. This project, _pysodium-cardano_, is a fork of pysodium with added wrappers for
the VRF functions present in the [Cardano-fork](https://github.com/IntersectMBO/libsodium) of libsodium.

## Building
This project uses the [hatch](https://hatch.pypa.io/1.9/) build system.

    hatch build

To run tests:

    hatch run test

## Installing the Cardano-Fork of libsodium

    git clone https://github.com/IntersectMBO/libsodium
    cd libsodium
    git checkout dbb48cc
    ./autogen.sh && ./configure
    make -j8
    make check
    make install
