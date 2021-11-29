# Install-cargo-Rice.
Install cargo Rice
cargo Rice my_project
cd my_project/contract
rustup install $(cat rust-toolchain)
rustup target add --toolchain=$(cat rust-toolchain) wasm32-unknown-unknown
cargo build --release
cd my_project/tests
cargo test
