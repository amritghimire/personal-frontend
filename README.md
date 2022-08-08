# Router Example

[![Demo](https://img.shields.io/website?label=demo&url=https%3A%2F%2Fexamples.yew.rs%2Frouter)](https://examples.yew.rs/router)

A blog all about yew.
The best way to figure out what this example is about is to just open it up.
It's mobile friendly too!

## Running

While not strictly necessary, this example should be built in release mode:

```bash
trunk serve --release
```

Content generation can take up quite a bit of time in debug builds.

## Concepts

This example involves many different parts, here are just the Yew specific things:

- Uses [`yew-router`] to render and switch between multiple pages.

The example automatically adapts to the `--public-url` value passed to Trunk.
This allows it to be hosted on any path, not just at the root.
For example, our demo is hosted at [/router](https://examples.yew.rs/router).

This is achieved by adding `<base data-trunk-public-url />` to the [index.html](index.html) file.
Trunk rewrites this tag to contain the value passed to `--public-url` which can then be retrieved at runtime.
Take a look at [`Route`](src/main.rs) for the implementation.

[`yew-router`]: https://docs.rs/yew-router/latest/yew_router/