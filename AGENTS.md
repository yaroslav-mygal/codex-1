# Repository Guidelines

## Project Structure & Module Organization

This repository is currently a clean workspace with no application source committed yet. As code is added, keep the layout predictable:

- `src/` for application or library source code.
- `tests/` for automated tests that mirror `src/` structure.
- `assets/` for static files such as images, fixtures, or sample data.
- `docs/` for design notes, architecture decisions, and user-facing documentation.
- Root-level configuration files only when they apply to the whole project.

Prefer small, focused modules. If a file grows to cover unrelated responsibilities, split it by feature or domain behavior rather than by generic utility buckets.

## Build, Test, and Development Commands

No project-specific build system is present yet. Add commands to the project manifest or `Makefile` when tooling is introduced, and keep this section updated.

Useful baseline checks:

- `find . -maxdepth 3 -type f` lists the current repository contents.
- `git status` checks pending changes once the directory is initialized as a Git repository.
- `npm test`, `pytest`, `go test ./...`, or similar should be documented here when the stack is chosen.

## Coding Style & Naming Conventions

Follow the conventions of the language and framework selected for the project. Keep formatting automated where possible, using tools such as Prettier, Black, rustfmt, or gofmt. Use descriptive names that reflect behavior:

- Files and directories: lowercase with hyphens or the language-standard style.
- Classes and types: `PascalCase`.
- Functions, variables, and test cases: clear action-oriented names.

Avoid broad helper modules until repeated patterns justify them.

## Testing Guidelines

Place tests in `tests/` or beside source files if that is idiomatic for the chosen stack. Name tests after the behavior under test, for example `test_user_can_create_project` or `createsProjectWithValidInput`. Cover core behavior, edge cases, and regressions introduced by bug fixes.

Document the exact test command here when test tooling is added.

## Commit & Pull Request Guidelines

There is no Git history available in this workspace, so no repository-specific commit convention can be inferred. Use concise imperative commit messages, for example `Add project scaffold` or `Fix parser validation`.

Pull requests should include a short summary, relevant issue links, test results, and screenshots or recordings for UI changes.
