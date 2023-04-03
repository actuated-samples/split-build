# split-build

Building multi-arch images with QEMU can be really slow.

Parca was taking 33 minutes, on an Arm host with actuated it took 1min 26s

VPP from Network Service Mesh failed after 6 hours, but with actuated and arm64 it took < 9 minutes

## How it works

* Two separate builds run on actuated runners for their native architecture with the name of the SHA plus a suffix of the architecture
* A final step runs at the end to publish a manifest with the name of the SHA

See also:

* [Bring Your Own Metal Case Study with GitHub Actions](https://actuated.dev/blog/case-study-bring-your-own-bare-metal-to-actions)
* [How to make GitHub Actions 22x faster with bare-metal Arm](https://actuated.dev/blog/native-arm64-for-github-actions)

