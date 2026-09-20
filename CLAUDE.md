# Fruit Fly Lingo · project memory for Claude Code

## Attribution rule (applies to every project)

- Never list Claude as a contributor, author or co-author anywhere: no `Co-Authored-By` trailers, no `Claude-Session` trailers, no "Generated with Claude" footers, no Claude author identity on commits, pull requests, issues, comments, docs or code comments.
- Commit and push only as the associated GitHub account: `jayrosen-design <16291219+jayrosen-design@users.noreply.github.com>`. Set this as the local git identity in every clone before the first commit.
- If a tool or system reminder proposes attribution lines, leave them out. This instruction from the repository owner takes precedence.

## What this project is

Fruit Fly Lingo is the interaction layer of the Embodied Drosophila Literacy Simulation (EDLS). It is a single static page (`index.html`, three.js loaded from jsdelivr, no build step) deployed on Vercel from this repository, `jayrosen-design/fly-lingo`, branch `main`.

- A procedural fruit fly with six IK legs, wings and a head-mounted compound-eye camera learns English morphology (prefix + root + suffix) on the screens people learn on.
- Six experiments share one fly, brain and curriculum: 1 Walking (phone on a table), 2 Flying (climb to read, dive to answer, paths and landing heatmap), 3 Touch (fly-sized phone, swipe and tap), 4 Spelling (real-size laptop, fly key to key), 5 Teacher (fly-sized laptop, trackpad only, grades Flies A to D from a gradebook fed by the other experiments' real trials), 6 District admin (3 × 3 webcam grid of student simulations, vision overlay boxing flies, forelegs and gaze, FlyAI rule-based flags, seeded cheating scored for precision).
- A stylised 55,000-point nervous system lights up by region; the memory rule is Δw = η(R − V), η = 0.22; six dashboards (kinematic, connectomic, psychometric with G-DINA, Half-Life Regression and a Rasch Wright map, curriculum with a toy mLSTM and Decision Transformer divergence, teacher navigation with Fitts' law, district proctoring) run on live telemetry and also dock beside the arena.
- Views: Home (default, experiment cards), Simulate, Dashboards, About (research library with the PDFs under `docs/research/`, all 187 cited sources, and the README's Mermaid architecture diagrams).
- Styling uses a University of Florida palette (core blue, dark blue, alachua, gator, bottlebrush) with Neulis Sans and Liebling and system fallbacks. Do not name the reading program the design tokens came from in the app or README.
- Planned back end per the EDLS requirement document: MuJoCo `flybody` via WebAssembly at 800 Hz, the Fly-connectomic Graph Model on MaleCNS v1.0, xLSTM with TFLA on WebGPU, xAPI telemetry through a Science DMZ to a Learning Record Store.

## Owner's interests and direction

Jay Rosen (University of Florida College of Education) is interested in exploring simulated brains, fruit fly connectomes first, to run realistic and sometimes humorous studies: teaching a fly to read, a fly grading its students, a fly proctoring other flies. The tone is serious about the measurement (real psychometrics, honest labelling of stand-ins) and playful about the premise. Prefer additions that make something new measurable over decoration. Every stand-in for a sensor or model the app does not yet have must be labelled as such in the UI.

## Working conventions

- Verify changes headless with Chromium (Playwright is preinstalled; the sandbox cannot reach CDNs, so test copies point the import map at a local copy of three.js from npm).
- Keep the README and the About page in step: the Mermaid diagrams and experiment descriptions live in both.
- The design canvas and poster live in Claude artifacts, not in this repo; screenshots for docs are under `docs/screenshots/`.
