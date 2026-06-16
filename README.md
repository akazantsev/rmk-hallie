# RMK for Hallie

Install rustup https://rustup.rs/

Pull in the environment variables for Rustup in the current terminal session:
```sh
. "$HOME/.cargo/env"
```

Install the toolchain:
```sh
rustup target add thumbv7em-none-eabihf
```

Install rmkit:
```sh
cargo install rmkit flip-link cargo-make
```

Build both firmwares
```sh
cargo build --release
```

or build them separately
```sh
cargo build --release --bin central
cargo build --release --bin peripheral
```

Convert firmwares for both parts to UF2.
```sh
cargo make uf2 --release
```
