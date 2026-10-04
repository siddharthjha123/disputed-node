# Quorum disputed Node.js demo

This repository explicitly opts into Quorum's allowlisted
`node-disputed-demo-v1` profile through `quorum-disputed-demo.json`.

The normal published `.tgz` is committed under `release-assets/published/`.
During independent rebuilding, the trusted demo profile adds a fresh nonce to
each builder's temporary copy before running `npm pack --ignore-scripts`.
The three resulting hashes therefore disagree, producing `DISPUTED`.

This is demonstration-only behavior. Repository lifecycle scripts remain
disabled, and the ordinary `node-package-v1` profile stays deterministic.
