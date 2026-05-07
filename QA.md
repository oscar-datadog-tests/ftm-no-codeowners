# QA card — ftm-no-codeowners

## Description

Same configuration as ftm-fully-protected-with-flakes, but the repo ships **without** a `.github/CODEOWNERS` file. Drives the §7.6 empty Code Owners card state.

## Audit cells exercised

- §7.6 empty state — "No code owners" pill + "Set up CODEOWNERS" CTA + body copy.

## Required Datadog toggles

| Toggle | State | Notes |
| --- | --- | --- |
| EFD | **on** | Repo settings |
| PR Gate | **on** | Source Code rule scoping this repo |
| ATR | **on** | Repo settings |
| Policies | **full** | Default 7-day quarantine policy on |

## Special setup steps

None — the absence of CODEOWNERS is the entire point.

## Expected verdicts (after warm-up)

- §7.6 Code Owners card: empty state. "No code owners" pill, body copy invites setting up CODEOWNERS.

## Readiness

T+14.

## How to refresh

```bash
git commit --allow-empty -m "rerun" && git push
```
