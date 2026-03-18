# Clean-Room Contracts

Recovered ABI contracts and validation helpers for the Coruna exploit chain. See the [top-level README](../README.md) for the full chain reconstruction.

## Contents

- `include/coruna_contracts.h` — record IDs, struct layouts, vtable definitions, command IDs
- `include/coruna_stage_loader.h` — loader-side record-store and worker-pack contracts
- `src/coruna_contracts.c` — parsing/validation helpers for selector and mode blobs, vtable wrappers
- `src/coruna_stage_loader.c` — record-store dedup/conflict logic, mode projection, worker-pack builder

## Verify

```sh
clang -std=c11 -Wall -Wextra -Werror -Iinclude -fsyntax-only src/coruna_contracts.c src/coruna_stage_loader.c
```
