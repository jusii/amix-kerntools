# CLAUDE.md — amix-kerntools

The **build hub** for a family of MIT-licensed Amiga UNIX (Amix — Commodore's SVR4.0 port to the
68030 Amiga) device drivers. It owns *how* an Amix kernel is built: it discovers sibling driver
repos by their `driver.conf`, generates the SCSI controller-selector wiring, applies each driver's
kernel patches, links the kernel, and runs a clean-gate that defeats an intermittent emulator
linker-corruption bug. It ships **no driver source** (those live in sibling driver repos) and **no
Amix** — builders bring their own licensed Amix 2.1 install.

See [`AGENTS.md`](AGENTS.md) for the driver-author contract and [`README.md`](README.md) for the
build how-to. [`REPOS.md`](REPOS.md) maps the driver ecosystem.

## Commit discipline

No AI attribution in commit messages — do not add `Co-Authored-By: …` or `Generated with …`
trailers.
