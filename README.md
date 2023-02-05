Arbitrary-precision arithmetic package for Elm

# harfangk/elm-bignum

Elm library for arbitrary-precision decimal arithmetic that supports basic arithmetic, comparison, and rounding operations.
I've forked this library from chain-partners/elm-bignum to update it as I've left that company in 2019 and no longer has access to the repository.

## Design Goals

I initially wrote this library because I needed division operation of big decimal numbers. My goal was to write a library that:

1. Supports basic arithmetic operations
2. Has okay performance on browser

## TODO

* Improve handling of fraction digits that are dropped off in `moveZeroesToE` function. They are currently being truncated but should be rounded.
* Get rid of `Maybe.withDefault` calls in Decimal module if possible.
* Improve performance, especially for division and square root operations.
* Add base conversion, including experimentation with changing default base to 2^26.
* Reimplement `toString` functions using `Parser` library.
* Find a better way to handle operations on last digits of `Significand` without relying on `Integer.toString`. Current implementation uses string manipulation using regular expression, as my initial implementation using recursion was crushingly slow. 
* Implement IEEE 754-2019 specifications.
