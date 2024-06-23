# `rust-short-lived-cache`

This GitHub Action sets up `actions/cache@v4` to temporarily cache build outputs from a Rust build. The idea here is not to speed up all runs, but only to pass build artifacts between different jobs in the same run.

One use-case for that is to build in a dedicated job, but then have tests and clippy and other things that depend on compiled outputs run in different jobs.
