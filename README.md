# rust-metaflac

A library for reading and writing FLAC metadata, modified for MoosicBox.

## Usage

Add the dependency to your `Cargo.toml`:

```toml
[dependencies]
moosicbox_metaflac = "0.1"
```

```rust
extern crate moosicbox_metaflac;

use moosicbox_metaflac::Tag;

fn main() {
	let tag = Tag::read_from_path("music.flac").unwrap();

	// Some things modifying the tag

	tag.save().unwrap();
}
```
