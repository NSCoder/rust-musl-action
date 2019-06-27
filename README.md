# GitHub Action for Rust and MUSL

Action provides an environment with Rust, MUSL and x86_64-unknown-linux-musl target.

## Usage

To compile a rust binary/library with x86_64-unknown-linux-musl target:

```hcl
action "build" {
  env = {
      BUILD_TARGET = "x86_64-unknown-linux-musl"
  }
  uses = "juankaram/rust-musl-action@master"
  args = "cargo build --target $BUILD_TARGET --release"
}
```

## Attribution

Heavily inspired by [GitHub Actions](https://github.com/actions), [Rust Action](https://github.com/icepuma/rust-action) and [David Lewis Work](https://github.com/davidarmstronglewis).

## License

The Dockerfile and associated scripts and documentation in this project are released under the [MIT License](LICENSE).

