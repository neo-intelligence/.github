# Contributing to Neo Intelligence repositories

## Pull request titles

Pull requests are squash-merged, so a PR's title becomes its one commit on `main`. Titles follow
[Conventional Commits](https://www.conventionalcommits.org/), with the ticket at the end:

```
<type>(<scope>): <what changes> (<TICKET>)
```

```
fix(booking): project list matches the main filter and sub-filter (CS-284)
feat(timesheets): company settings for split days (NEO-4450)
refactor(pay)!: payroll legs move under timesheet blocks (NEO-4148)
```

| Type | For |
|---|---|
| `feat` | something new people can use |
| `fix` | a bug fix |
| `perf` | faster or lighter, same behaviour |
| `refactor` | restructured code, same behaviour |
| `test` | tests only |
| `docs` | documentation only |
| `build`, `ci` | builds, dependencies, pipelines |
| `chore` | anything else that doesn't change behaviour |
| `revert` | undoing an earlier change |

- **Scope** is the domain the change is in (`pay`, `booking`, `timesheets`, `integrations`…), the same names as the
  architecture's domain map.
- **`!`** after the scope marks a breaking change: an API contract, the database, or behaviour others rely on. Say what
  breaks and how to roll back in the PR's "Deployment and rollback" section.
- Commits inside a PR can be anything: only the title is kept.

## Pull request descriptions

Every repository uses the same template (`.github/pull_request_template.md` in this repository): what and why,
screenshots, how you tested it, deployment and rollback, notes for reviewers, and a short checklist. A line or a link per
item is enough.
