Guidance for Claude Code sessions working in this repo. Read [MEMORY.md](MEMORY.md) for full project history and current state before making non-trivial changes — it explains *why* things are the way they are, which this file doesn't repeat.

## What this project is

This is Anurag Gurumurthy's GitHub profile repo — a repo named exactly the same as his GitHub username (`anuraggurumurthy`), which GitHub renders specially as the profile README on his GitHub profile page. It is not an application: there is no build, no runtime, no tests, and no source code to compile. The content that matters is `README.md`, which GitHub displays directly. Supporting files are `banner.png` (image embedded in the README) and `AnuragResume.pdf` (linked from a badge in the README). There is also a `.github/workflows/release.yml` that auto-tags and publishes a GitHub release on every push to `main`, and a `release notes/Latest Release.txt` file plus `scripts/StartService.bat` / `scripts/StopService.bat` that appear to control a local Windows service (also named `anuraggurumurthy`) used to auto-commit/update that release notes file — see MEMORY.md for what's actually known about this.

## Things to preserve

- The overall structure and tone of `README.md` (intro/"Whoami" section, Socials, Tech Stack, Payments) and its use of shields.io badges and emoji headers — this is a stylistic profile README, not prose to be "cleaned up."
- The resume badge link, which points to the raw GitHub URL for `AnuragResume.pdf` at `main` — if the PDF is renamed or moved, this link must be updated in the same change.
- `banner.png` embed at the top of the README (width/height attributes as-is).
- The `.github/workflows/release.yml` auto-tagging/release workflow — don't alter its tagging or pruning logic without understanding it explains itself well enough, but treat it as intentional automation, not dead config.

## Commands to run before considering a change done

None. There is no build, lint, or test tooling in this repo.
