# cargo-bump

> **NOTE**: I've forked this because the original version was not *Ideal*,
> to say the least.
> 
> This version adds a tag automatically, and tags with the format `v*`, so for example `v0.1.0`.

This adds the command `cargo bump` which bumps the current version in your
`Cargo.toml`.

## installation

Clone this repo with `git`, then `cd` into the directory and just install this thingy with:

```shell
cargo install --path .
```

And *away* you go.

## examples

Increment the patch version: `cargo bump` or `cargo bump patch`

Increment the minor version and create a git tag: `cargo bump minor --git-tag`

Set the version number directly: `cargo bump 13.3.7`

## usage

```
USAGE:
    cargo bump [FLAGS] [<version> | major | minor | patch]

FLAGS:
    -h, --help       Prints help information
    -v, --version    Prints version information
    -g, --git-tag    Commits the new version and creates a git tag

ARGS:
    <version>    Version should be a semver (https://semver.org/) string or the
                 position of the current version to increment: major, minor or patch.
```
