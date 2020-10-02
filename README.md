# FRAME pallet for trading magical artwork

## Purpose

This pallet allows for magical art be conjured by witches/wizards/elves/other magical creatures, and be traded and collected by muggles/no-maj and other communities between different planets.  Unlike [conjuration]i(https://harrypotter.fandom.com/wiki/Conjuration) one might have learnt, the artwork conjured in this pallet will not reversely transfigurable, according to the muggle's study of cryptographic immutibility.
## Dependencies

This pallet depends on [substrate-ipfs]() for interplanetary storage 

### Traits

This pallet does not depend on any externally defined traits.

### Pallets

This pallet [pallet-nft](https://github.com/danforbes/pallet-nft) for the tokenization of the non-fungible nature of the art work.

## Installation

### Runtime `Cargo.toml`

To add this pallet to your runtime, simply include the following to your runtime's `Cargo.toml` file:

```TOML
[dependencies.mugwort-art]
default_features = false
git = 'https://github.com/whalelephant/mugwort-art.git'
```

and update your runtime's `std` feature to include this pallet:

```TOML
std = [
    # --snip--
    'mugwort-art/std',
]
```

### Runtime `lib.rs`

You should implement it's trait like so:

```rust
/// Used for test_module
impl example_pallet::Trait for Runtime {
	type Event = Event;
}
```

and include it in your `construct_runtime!` macro:

```rust
ExamplePallet: substrate_pallet_template::{Module, Call, Storage, Event<T>},
```

### Genesis Configuration

// TODO 

## Reference Docs

You can view the reference docs for this pallet by running:

```
cargo doc --open
```

