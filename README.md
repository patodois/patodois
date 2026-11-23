# patodois

Open-source game tooling in Rust: readers for game data, a clean-room engine
reimplementation, and a protocol for running one game inside another. Every
repository reads **your own install**; none contains game data or decompiled
code. Each one has an `AGENTS.md` with its rules and a README that says where
the work stops, so a person or an AI agent can pick it up.

Much of this code is written with AI assistance (Claude), directed and reviewed
step by step.

## Fallout 4 engine in Rust (Bethesda Creation Engine)

| Repository | What it is |
|---|---|
| [osp-fo4](https://github.com/patodois/osp-fo4) | Clean-room reimplementation of Fallout 4's engine: BA2, ESP/ESM, NIF, Havok and Papyrus readers, CPU renderer, GPU viewer, walking, and a script VM that runs the opening quests. Not playable yet; milestones in `docs/next-steps.md`. MIT OR Apache-2.0. |
| [osp-f4se-measure](https://github.com/patodois/osp-f4se-measure) | F4SE plugin and measurement packets: owners of the game measure its behaviour so osp-fo4's pending rules can be confirmed. |

## Cross-game passthrough (game mash-ups and crossovers)

| Repository | What it is |
|---|---|
| [rewrite-bridge](https://github.com/patodois/rewrite-bridge) | The protocol: one game hosted inside another on one machine, sharing players, poses, spawns, collision and depth. Start here. |
| [link-c](https://github.com/patodois/link-c) · [link-cs](https://github.com/patodois/link-cs) · [link-java](https://github.com/patodois/link-java) | The protocol as a single-header C99 library (SKSE, F4SE, ScriptHookV), a C# library (Unity, BepInEx, MelonLoader) and a Java 8 library. |
| [minecraft-link](https://github.com/patodois/minecraft-link) | Minecraft client mod speaking the protocol (Fabric, NeoForge, Forge, Quilt). |
| [bridge-guest](https://github.com/patodois/bridge-guest) | Renders any provider's model into any host game with the host's camera and depth. |
| [crossover](https://github.com/patodois/crossover) | A War Thunder level and tank with a Warframe character in one Bevy scene. |
| [bridge-testbed](https://github.com/patodois/bridge-testbed) · [bridge-live](https://github.com/patodois/bridge-live) | Test scenes and a live interop matrix for the protocol. |

## Game data readers and extractors (Rust, glTF export)

| Repository | Game or format |
|---|---|
| [wt-unpack](https://github.com/patodois/wt-unpack) · [wt-formats](https://github.com/patodois/wt-formats) | War Thunder (Dagor Engine): vromfs, BLK, DXP, GRP, models, skeletons. |
| [wf-unpack](https://github.com/patodois/wf-unpack) | Warframe (Evolution Engine) cache packages. |
| [mc-unpack](https://github.com/patodois/mc-unpack) | Minecraft: Java Edition block and item models. |
| [hytale-unpack](https://github.com/patodois/hytale-unpack) | Hytale models, animations and prefabs. |
| [nocturne-unpack](https://github.com/patodois/nocturne-unpack) · [unity-bundle](https://github.com/patodois/unity-bundle) | Shin Megami Tensei III Nocturne HD; UnityFS asset bundles. |
| [bcn-decode](https://github.com/patodois/bcn-decode) | BC1 to BC7 texture decoder, `no_std`. |
| [lztans](https://github.com/patodois/lztans) | Clean-room decoder for Kraken, Mermaid/Selkie and Leviathan streams. |

## Controllers on macOS

| Repository | What it is |
|---|---|
| [gip-pad](https://github.com/patodois/gip-pad) | Wired Xbox One/Series (GIP) controllers on macOS through libusb. |
| [gip-xinput](https://github.com/patodois/gip-xinput) | XInput for Wine on macOS on top of gip-pad. |

None of these projects is affiliated with or endorsed by the games' publishers.
