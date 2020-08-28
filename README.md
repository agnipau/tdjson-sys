# tdjson-sys

For instructions on how to build TDLib, refer to the [official indications](https://github.com/tdlib/td#building).

After you've built the library, you need to install it on your system:

```bash
# Run the following line as root
cmake --build . --target install
```

Finally make sure that your `$LD_LIBRARY_PATH` includes /usr/local/lib or
whatever location you've installed TDLib.

## Alternatives

Before writing this I tried:

```toml
# Compiling syntex_syntax v0.58.1
# error[E0423]: expected function, tuple struct or tuple variant, found struct `ast::Name`
tdjson-sys = "0.1.5"

# error: failed to select a version for the requirement `bindgen = "^0.54.1"`
#   candidate versions found which didn't match: 0.55.1, 0.55.0, 0.54.0, ...
#   location searched: crates.io index
# required by package `tdjson-sys-copy v0.1.0`
tdjson-sys-copy = "0.1.0"
```

All of which got me compilation errors. Probably in the future these problems
will be fixed but I needed something that worked now.

#### License

<sup>
Licensed under either of <a href="LICENSE-APACHE">Apache License, Version
2.0</a> or <a href="LICENSE-MIT">MIT license</a> at your option.
</sup>

<br>

<sub>
Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in this crate by you, as defined in the Apache-2.0 license, shall
be dual licensed as above, without any additional terms or conditions.
</sub>

