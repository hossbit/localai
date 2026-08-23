# Tracked upstream versions

Weekly record of the llama.cpp / llama-swap versions actually resolved by this
project. localai.conf pins both to `latest`; this file documents what that
resolved to each week. Updated by the weekly update cycle (Sunday).

| Week (Sun -> Sun) | Change | llama.cpp | llama-swap | Backend | Updated |
|---|---|---|---|---|---|
| 2026-08-23 -> | llama.cpp started publishing stable `vX.Y.Z` releases alongside the existing `b[NUM]` bleeding-edge builds (v0.2.0 published 2026-08-21; see https://github.com/ggml-org/ggml/discussions/1579). Because `vX.Y.Z` releases are non-prerelease, GitHub's `/releases/latest` now resolves to them instead of the newest `b[NUM]` build, and they ship no binaries of their own (only a `nightly-tag.txt` pointer to the corresponding `b[NUM]` release). Added `LLAMA_CPP_CHANNEL` (`bleeding-edge`\|`stable`) plus channel-aware release resolution (`resolve_llama_cpp_latest_json`, `resolve_llama_cpp_binary_json` in lib/install.sh) so `LLAMA_CPP_VERSION=latest` keeps tracking `b[NUM]` by default and can opt into the `vX.Y.Z` channel instead. llama.cpp: b10453 -> b10603; llama-swap: v250 -> v251. | b10603 | v251 | cuda | 2026-08-23 |
| 2026-08-16 -> 2026-08-23 | llama.cpp: b10410 -> b10453 (CUDA source build, commit 3cb7ffb); llama-swap: v249 -> v250 (60226b6) | b10453 (3cb7ffb) | v250 (60226b6) | cuda | 2026-08-16 |
| 2026-08-09 -> 2026-08-16 | (baseline) | b10410 (154d57a) | v249 (f94c94a) | cuda | 2026-08-13 |
