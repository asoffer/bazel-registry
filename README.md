# Bazel Registry

This repository is a registry of bazel components that are not sufficiently
stable to push to the central Bazel Repository, but that I use frequently and
want to have easily accessible.

## Usage

In your `.bazelrc`, make sure this repository is accessible. You can do this by
adding the following to your `.bazelrc`:

```
common \
  --experimental_enable_bzlmod \
  --registry=https://raw.githubusercontent.com/asoffer/bazel-registry/main \
  --registry=https://bcr.bazel.build
```

Note that Bazel uses the Bazel Central Repository (BCR) by default, but when
specifying a repository explicitly, the BCR is disabled. Thus, to enable it as a
backup, it must be specified explicitly.

If you have other registries to be accessed, they can be added with additional
`--registry` tags and ordered as desired.
