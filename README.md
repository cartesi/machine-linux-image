# Cartesi Machine Linux Image

The Cartesi Machine Linux Image is the repository that provides the Docker configuration files to build the Linux kernel `linux.bin` image. This is used to run a Linux environment on the Cartesi Machine Emulator reference implementation. The `linux.bin` is built from the Linux source, targeting `riscv64`.

## Getting Started

### Requirements

- Docker >= 18.x
- GNU Make >= 3.81

### Build

```bash
$ make build
```

If you want to tag the image with custom name you can do the following:

```bash
$ make build TAG=mytag
```

To remove the generated images from your system, please refer to the Docker documentation.

#### Development

There is a separate `build.mk` Makefile that can be used for kernel for development.

```bash
$ make -f build.mk clone
$ make -f build.mk run
$ make -f build.mk
```

There is also a `run-selftest` target to run the kernel tests.
To use it, run:

```bash
$ make -f build.mk run-selftest
```

#### Makefile targets

The following options are available as `make` targets:

- **build**: builds the docker linux-kernel image
- **copy**: builds the docker linux-kernel image and copy it's artifact to the host

## Contributing

Thank you for your interest in Cartesi! Head over to our [Contributing Guidelines](CONTRIBUTING.md) for instructions on how to sign our Contributors Agreement and get started with Cartesi!

Please note we have a [Code of Conduct](CODE_OF_CONDUCT.md), please follow it in all your interactions with the project.

## Authors

See [AUTHORS](AUTHORS) file.

## License

The image-kernel repository and all contributions are licensed under
[APACHE 2.0](https://www.apache.org/licenses/LICENSE-2.0). Please review our [LICENSE](LICENSE) file.
