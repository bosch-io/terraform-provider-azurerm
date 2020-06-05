# Build instructions (CIAM User Hub)

For changes to the Terraform provider, *first* decide on which release you will base your implementation.

* Create a feature branch based on the selected (upstream) release branch e.g. `release/v2.12.0`.
* Copy the `azure-pipelines.yml` over from the last successfully built release branch.
* Make your implementation changes.
* Add the release version together with a extension `-v0` to `version/version.go` (e.g. `2.12.0-v0`).
* Set the pipeline variable `release_branch` to the release version, e.g. `v2.12.0`.
* Create a PR from your feature branch into the release branch.
