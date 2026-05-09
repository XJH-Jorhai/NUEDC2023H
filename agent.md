# Agent Project Notes

## Project Identity

This repository is a complete, open-source solution project for Problem H of the 2023 National Undergraduate Electronics Design Contest in China.

The project is expected to collect three kinds of deliverables:

1. Solution design documents for the contest problem.
2. Hardware materials designed for the solution.
3. STM32 microcontroller firmware used by the solution.

Use `docs/`, `hardware/`, and `software/` as the canonical top-level directories. If older notes mention `docx/`, treat that as `docs/` unless the maintainer explicitly requests a separate directory.

## Directory Contract

### `docs/`

Use this directory for documentation and reference material:

- original contest problem statement
- Markdown write-up for the solution
- design-related reference material, such as module manuals and datasheets
- LaTeX template for the final design report

Keep generated build artifacts out of version control unless they are explicitly needed for review or release.

### `hardware/`

Use this directory for hardware-related content:

- module connection descriptions
- schematic design files
- PCB or hardware notes if later added
- supporting files needed to reproduce the hardware design

Prefer source design files over exported images or PDFs when both are available. Exports may be committed only when they help readers inspect the design without the original EDA tool.

### `software/`

Use this directory for firmware:

- STM32F407 firmware derived from <https://github.com/XJH-Jorhai/FK407-template>
- project-specific drivers, application code, and build configuration
- notes needed to build, flash, or debug the firmware

Keep the relationship with the upstream FK407 template clear when importing or modifying template files.

## Maintenance Rules

- Keep changes scoped to the requested task.
- Do not fill placeholder content just to make directories look complete.
- Do not move files across `docs/`, `hardware/`, and `software/` unless their purpose clearly belongs elsewhere.
- Prefer reproducible source files over screenshots or binary-only exports.
- When adding documentation, keep reader-facing explanations in `README.md` or files under `docs/`; keep agent-only workflow notes in this file.
- When adding firmware, document required toolchains and board assumptions near the firmware source.
- When adding hardware files, document the EDA tool and version when it matters for compatibility.

## Verification Expectations

- Documentation changes should be checked for clear paths, consistent terminology, and readable Markdown.
- Firmware changes should be built or otherwise verified with the available STM32 toolchain.
- Hardware changes should include enough source material for another contributor to inspect or reproduce the design.
