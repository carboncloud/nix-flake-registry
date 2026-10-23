# Our Nix flake registry

To pin to the latest versions

## Nixpkgs

```
nix registry pin --registry ./flake-registry.json nixpkgs github:NixOs/nixpkgs/release-26.05
```

## flake-utils

```
nix registry pin --registry ./flake-registry.json flake-utils github:numtide/flake-utils/main
```

# Bug in recent versions of `nix`!

The bug causes `nix registry pin` to replace, rather than add, the entry. So some care has to be taken to make sure that both entries remain after an update.

You can read more [here](https://github.com/NixOS/nix/issues/15540).
