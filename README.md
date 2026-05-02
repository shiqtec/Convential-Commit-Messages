# Git Commit Message Instructions

Use Conventional Commits v1.0.0.

Generate a clear, concise commit message based only on the staged diff.

## Format

Subject line, required:

```text
<type>(<scope>): <summary>
```

Then:

- Add a blank line after the subject.
- Add a body only when it adds useful context.
- Body must be 1–6 bullet points describing what changed and why.
- Use present tense and imperative voice.
- Add a footer only when needed.

## Allowed Types

Use one of the following types:

- `feat` — new feature
- `fix` — bug fix
- `docs` — documentation changes
- `style` — formatting, linting, whitespace, or code style only
- `refactor` — code restructuring without behavior changes
- `perf` — performance improvement
- `test` — adding or updating tests
- `build` — build system, tooling, or dependency changes
- `ci` — CI/CD configuration or pipeline changes
- `chore` — routine maintenance or minor non-functional changes
- `revert` — reverting a previous commit
- `hotfix` — urgent production bug fix
- `security` — security vulnerability fix
- `release` — version bump, release preparation, or tagging

## Scope Rules

- Pick a short scope from the codebase when clear.
- Examples: `api`, `sync`, `sftp`, `db`, `auth`, `ui`, `config`, `email`, `pdf`, `tests`.
- Omit the scope if it is unclear.
- Do not invent a scope that is not supported by the diff.

## Subject Rules

- Keep the subject line 72 characters or fewer.
- Use lowercase type and scope.
- Use imperative voice.
- Do not end the subject with a period.
- Summarize the main intent of the change, not just the files changed.

## Body Rules

- Add a body only when the change needs explanation.
- Use bullet points only.
- Write 1–6 bullet points.
- Explain what changed and why, based on the diff.
- Do not describe obvious file-level changes unless they matter.
- If the reason for the change cannot be inferred, add this as the final body bullet:

```text
- Why: <fill in>
```

## Footer Rules

- Include `BREAKING CHANGE: ...` when the change is breaking.
- Include ticket references such as `ABC-123` if present in the branch name, code, comments, or diff.
- Do not invent ticket references.

## Examples

```text
feat(auth): add user login functionality
```

```text
fix(ui): correct mobile header alignment
```

```text
docs: update README setup instructions
```

```text
refactor(api): extract authentication logic

- Move token validation into a dedicated service.
- Reduce duplication across protected endpoints.
- Keep existing authentication behavior unchanged.
```

```text
perf(db): cache frequently used lookup data

- Add in-memory caching for reference data.
- Reduce repeated database reads during request processing.
```

```text
security(auth): sanitize registration input

- Validate user-provided registration fields before processing.
- Prevent unsafe values from reaching authentication logic.
```

```text
revert: remove dark mode implementation
```

## Output Rules

Return only the commit message text.

Do not include explanations, markdown formatting, code fences, alternatives, or commentary.
