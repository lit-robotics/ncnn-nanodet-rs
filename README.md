# ncnn-nanodet-rs

Rust crate for the [nanodet](https://github.com/RangiLyu/nanodet) object detection model, based on [ncnn](https://github.com/Tencent/ncnn) neural network framework.

**Deprecated in favor of [nanodet-rs](https://github.com/lit-robotics/ncnn-nanodet-rs), which supports multiple neural network backends in addition to `ncnn`**

## Usage

Can be used as library by including in `Cargo.toml`:
```yaml
ncnn-nanodet-rs = { git = "https://github.com/chemicstry/ncnn-nanodet-rs" }
```

For rust-flavored usage see [examples/image.rs](examples/image.rs), or if you like opencv check [examples/opencv.rs](examples/opencv.rs)

## Cargo Features

- `image` for [image](https://crates.io/crates/image) based utility functions.
- `opencv` for [opencv](https://crates.io/crates/opencv) based utility functions.


## Running examples

Run pretrained COCO model on an image with rust image pipeline:
```bash
cargo run --example image --release --features image -- data/coco_test.jpg
```

Run pretrained COCO model on an image with opencv image pipeline:
```bash
cargo run --example opencv --release --features opencv -- data/coco_test.jpg
```
