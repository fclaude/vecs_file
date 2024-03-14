# Vecs_file

Crate for reading the format used for [DEEP1B](http://sites.skoltech.ru/compvision/noimi/).

## Usage

Read a file with `read_vecs_file`. You can read `i32`, `f32` and `u8` vecs files.

```rust
vecs_file::read_vecs_file::<i32>(path_to_file);
```

`read_vecs_file` returns a `Result` that is either a structure called `Vectors<T>` of a `VecsError`. The `Vectors<T>` structure implements functions to access individual vectors.

The crate also provides utility functions to write a vecs file, and a reader/writer from a stream. This allows reading/writing by blocks if needed.
