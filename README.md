# Test Kubernetes Build Product

E2E test repo for `kubernetes-product-build` workflow in buildon-github-actions.

Aggregates four same-org bundles (short-form refs) plus one cross-org vendor entry (full-form ref with a `vendor/` namespace prefix). Exercises Maven-style version range resolution, byte-identical defaults merging across bundles, and the `spec.contents` content list in the GitHub release notes. `allowLocalDefaultsOverride: false` enforces the strict path: any local default in `src/defaults/` must be byte-identical to its bundle-contributed counterpart or the build fails.
