# Moras Triage — public status

Auto-published status page for a **private** local-first email triage assistant
running on one Mac. Regenerated and pushed by the triage cycle itself.

**[View the dashboard →](https://troykyo.github.io/triage-stats/)**

## What is here

| File | Contents |
|---|---|
| `index.html` | The status page (self-contained, no external assets) |
| `stats.json` | The same figures, machine-readable |

## What is deliberately *not* here

This repository is public, so it carries **aggregate numbers only** — message
volumes, counts by priority, routing ratios, token totals and cost.

It contains no senders, no subjects, no addresses, no message or draft text, no
reminders, no VIP list, and no per-account breakdown. Those live only in a
git-ignored folder on one machine and are never transmitted anywhere.

The generator builds every published value through numeric coercion, so no
string read from mail can reach these files, and its test suite asserts that
against adversarial fixtures. The assistant it reports on never sends email
automatically, and composes sensitive or injection-flagged mail entirely
on-device.
