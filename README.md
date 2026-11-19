# vrout-core

Windows x64 build of official MetaCubeX/mihomo for vrout.

The workflow checks the latest stable upstream release every six hours. It applies
the vrout DNS and startup patch, runs Go tests, builds with `with_gvisor`, and
publishes only after those steps succeed. A patch or test failure leaves the
last release available to clients.

Each release includes the Windows executable, the corresponding patched source
archive, and the patch. Tag format is `v<upstream>-vrout.<patch revision>`.
Increment the patch revision in the workflow when publishing a new build of
the same upstream version.
