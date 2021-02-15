# U128

MSVC doesn't support __uint128_t / unsigned __int128 yet, as anyone who's tried to port code from Clang or GCC can attest. This class implements all the basic and not-so-basic functionality of an unsigned 128-bit integer that behaves like `__uint128_t`. You can `typedef` or `using` it and it should be a solid drop-in replacement.

Implemented in a single header, cpp, and (optionally) NatVis for debugging.

Fast, efficient implementation for modern x86, however the performance is somewhat worse than GCC or especially Clang due to a combination of MSVC's poor codegen and its dumb calling convention. Implementation attempts to work around these shortcomings as much as possible.
