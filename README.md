papi-rs
========

## Usage

First, add the following to your `Cargo.toml`:

```toml
[dependencies]
papi = "0.1.0"
```

Next, add this to your crate root:

```rust
extern crate papi;
```

Before building, ensure that PAPI is installed on your system.

## What is papi-rs?

The purpose of this crate is to provide Rust-idiomatic, easy-to-use PAPI bindings.
PAPI is a library that provides a consistent interface to hardware performance
counters. Visit the [PAPI website](http://icl.utk.edu/papi) for more information.

Note that this crate does not provide a high-level interface to PAPI.

## Environment Variables

There are two environment variables to specify custom PAPI library dependency:
- `PAPI_LIBRARY`: used for `-L` option
- `PAPI_INCLUDE_DIR`: used for `-I` option

Let's assume you installed PAPI in `/opt/papi/5.7.0/`, then you will run,
```bash
$ PAPI_LIBRARY=/opt/papi/5.7.0/lib/ PAPI_INCLUDE_DIR=/opt/papi/5.7.0/include/ cargo build
```

## Versions

This library targets the current Rust stable release,
and is currently tested with PAPI version 5.6.0.

## Platforms

The following platforms are currently tested:

* `x86_64-unknown-linux-gnu`
* `powerpc64le-unknown-linux-gnu`
