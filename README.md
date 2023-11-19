# vcv-rack-sdk

⚠️ Do not clone this repository or add it as a submodule. We could modify it whenever we see fit ⚠️

This repository is a mirror of the [VCV Rack SDK](https://vcvrack.com/downloads/).

It is meant only to be used as a dependency for the
[`eurorack-blocks`](https://github.com/ohmtech-rdi/eurorack-blocks) project.

This repository is not the official VCV Rack SDK repository. It exists only because VCV
Rack doesn't provide a repository for their SDK, and including it as a submodule of the
[`eurorack-blocks`](https://github.com/ohmtech-rdi/eurorack-blocks) project simplifies
installation and automations.

Always refer to the official source.

This repository is currently using
**version 2.4.0** of the VCV Rack SDK, with the following modifications:
- The `lin` (Linux), `mac` (macOS), `win` (Windows) variants of the SDK have been
   unified into one,
- Since the only difference (apart from the compiled libraries) between the
   different SDK variants are all in `openssl`, which itself is a dependency of
   `curl`, which eurorack-blocks doesn't use (or support), and neither the SDK
   files are including `curl`, we are removing those 2 dependencies all together,
- The compiled libraries have been organised by OS and CPU architecture.
