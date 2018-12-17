# CCP QUIC Datapath

This repository provides a patch for Google's implementation of QUIC that
allows QUIC to be used as a CCP datapath.

Follow the instructions below to setup this datapath, then see our
[guide](https://ccp-project.github.io/guide) to get started using CCP.

## Setup

1. Follow instructions at [https://chromium.googlesource.com/chromium/src/+/master/docs/linux_build_instructions.md to build and checkout Chromium in Linux].

2. After downloading and setting up Chromium, checkout commit hash `dedfa29047`.

3. Apply the patch file here with: `git apply quic-ccp.patch`

4. Run `git submodule update --init --recursive` in order to clone `libccp` into the right location.

5. In chromium/src, build the toy client and server `ninja -v -d explain -C BUILD_DIR quic_server quic_client`.
