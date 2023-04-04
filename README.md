# Guest Method ID Mismatch Reproduction

## Reproduction

Build `factors`

```
// in ./factors/
cargo build
```

Build `factors-wasm`

```
// in ./factors-wasm/
cargo build --target wasm32-unknown-unknown
```

Grep occurences of `MULTIPLY_ID`

```
// in root folder
grep -r 'pub const MULTIPLY_ID:' . | sed 's/:.* = \[/: \[/'
```
