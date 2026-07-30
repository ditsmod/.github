# Contributing to Ditsmod

Thank you for your interest in contributing to Ditsmod! 🎉  
Every contribution — whether it's a bug report, a documentation fix, or a new feature — is greatly appreciated.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Ways to Contribute](#ways-to-contribute)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Running Tests](#running-tests)
- [Pull Request Guidelines](#pull-request-guidelines)
- [Git Commit Message Conventions](#git-commit-message-conventions)

## Code of Conduct

Please be respectful and constructive in all interactions. This project follows the Contributor Covenant. By participating, you agree to uphold a welcoming and harassment-free environment for everyone.

## Ways to Contribute

- **Report bugs** – Open a GitHub Issue in the relevant repository with a clear description and reproduction steps.
- **Suggest features** – Open an issue tagged `enhancement` to discuss ideas before implementing.
- **Fix bugs or add features** – Pick up an existing open issue (look for `good first issue` or `help wanted` labels).
- **Improve documentation** – The main documentation lives in the [ditsmod/ditsmod](https://github.com/ditsmod/ditsmod) repository under the `website` directory.

> [!NOTE]
> Please open or comment on an issue before submitting a non-trivial PR so we can discuss the approach and avoid wasted effort.

## Development Workflow and Testing

Since the Ditsmod organization contains multiple repositories, each project may have its own specific development environment, build tools, and testing procedures. 

Please refer to the `README.md` or a local `CONTRIBUTING.md` (if present) in the specific repository you are working on for instructions on how to:
- Install dependencies
- Build the project
- Run tests and linters

> [!IMPORTANT]
> Make sure all local tests pass before submitting a Pull Request.

## Pull Request Guidelines

1. **Branch off `main`** — create a feature branch: `git checkout -b feat/my-feature`.
2. **Keep PRs focused** — one logical change per PR makes review easier.
3. **Write or update tests** for any changed behavior.
4. **Update documentation** if your change affects the public API.
5. **Ensure CI passes** — the build, linting, and tests must all be green.
6. **Fill in the PR description** — describe what changed and why, and link the related issue if applicable.

## Git Commit Message Conventions

We use **Conventional Commits** for all commits. A pre-commit hook (via Husky and commitlint) is configured to validate your commit message format before allowing a commit to be created.

### Format

Every commit message must follow this structure:

```text
<type>(<scope>): <description>
```

#### 1. Allowed Types (`<type>`)

Common types from Conventional Commits:

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation-only changes
- `style`: Changes that do not affect the meaning of the code (white-space, formatting, etc.)
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `build`: Changes that affect the build system or external dependencies
- `ci`: Changes to our CI configuration files and scripts
- `chore`: Other changes that don't modify src or test files

#### 2. Allowed Scopes (`<scope>`)

The scope depends on the specific repository you are contributing to:

- **For monorepos (like `ditsmod/ditsmod`)**: Use the package folder name (e.g., `core`, `router`, `cors`).
- **For single-package repositories**: The scope might be related to specific components, configurations (e.g., `ci`, `deps`), or omitted if the repository maintainers allow it.

Check the repository's commit history for examples of commonly used scopes.

### Examples

- **Valid commits:**
  - `feat(core): add new DI features`
  - `chore(deps): update dependencies`
  - `chore(ci): configure GitHub Actions`
  - `fix(router): resolve route matching bug`

- **Invalid commits (will be rejected by linters if configured):**
  - `chore: update dependencies` (if the repository requires a scope)
  - `Added new feature` (does not follow Conventional Commits format)
