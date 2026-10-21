# MEMORY — brbseq-tools

## Now / Next

- **Now (2026-10-21):** issue #1 (post-migration cleanup after the rename
  `BRBseq-tools` -> `brbseq-tools`) is done on branch
  `1-post-migration-cleanup-finish-what-the`. The PR says `Closes #1`.
- **Next:** merge the PR after Stephane says yes, then delete the branch.
- **Open, not ticketed:** `main` has two repository rulesets, 22117513 and
  23419165, with the same rules (`deletion`, `non_fast_forward`). One of them
  is probably a duplicate. Decide with Stephane before you delete one.

## Facts

- Plain script collection (R, bash) for BRB-seq data from the AVITI instrument.
  No build, no CI, no Docker image.
- Default branch is `main`. No GitHub Pages site. No self-hosted runner.
- Licence: GPL-3.0 (`LICENSE`).

## Verify commands

```bash
grep -rIn --exclude-dir=.git -e "BRBseq-tools" .            # must print nothing
gh api repos/Nucleomics-VIB/brbseq-tools/rules/branches/main --jq '[.[].type]'
```
