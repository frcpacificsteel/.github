# Collaboration guide

## The fast loop

1. A team member files a feature request, bug report, or test result with evidence.
2. A programming lead triages it: clarify the outcome, set labels and priority, then either close it, split it, or turn it into a ready task.
3. The assignee links their pull request to the issue and keeps the issue updated if the scope changes.
4. A reviewer verifies the stated validation. For robot-impacting changes, the pull request records the safe physical test conditions.
5. Merge only when the acceptance checks are met; create separate follow-up issues rather than quietly expanding scope.

## Triage expectations

- Use `status: needs triage` for new reports, `status: ready` once the outcome and acceptance checks are clear, and `status: blocked` when outside input is needed.
- Apply one `type:` label and any relevant area labels. Add `priority: critical` only for safety or match-blocking problems.
- Prefer a short screen recording, Driver Station log, photo, or exact reproduction sequence over a long narrative.
- Keep one issue to one decision or behavior. Link related work instead of combining unrelated requests.

## Pull request expectations

- Link the issue with `Closes #123` when the PR completes it.
- Describe user-visible behavior and the validation you actually performed; unchecked validation is intentionally not evidence.
- Request review from someone familiar with the changed subsystem. Do not self-merge robot-impacting changes unless the team has an explicit exception.
- Re-test on the robot after merges that affect controls, autonomous behavior, safety, CAN configuration, or deploy assets.

## Suggested labels

Create these once in each repository using GitHub's Labels settings. GitHub issue forms apply the names exactly.

| Group | Labels |
| --- | --- |
| Type | `type: bug`, `type: feature`, `type: task`, `type: test` |
| Status | `status: needs triage`, `status: ready`, `status: in progress`, `status: blocked`, `status: needs review` |
| Priority | `priority: critical`, `priority: high`, `priority: normal`, `priority: low` |
| Areas | `area: auto`, `area: controls`, `area: drivetrain`, `area: vision`, `area: safety`, `area: infrastructure` |

Issue forms, this guide, and the PR template are organization defaults when this repository is named `.github`. Repository-specific templates take precedence.
