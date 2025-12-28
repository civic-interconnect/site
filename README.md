# Site: Civic Interconnect

> Documentation site for Civic Interconnect.
> This repository is docs-only and does not publish a Python package.


## Install

- uv
- VS Code (recommended)

## One-Time Setup

Create a local environment and install dependencies.

```shell
uv self update
uv python pin 3.12
uv venv

# Windows:
.venv\Scripts\activate

# macOS/Linux:
# source .venv/bin/activate

uv sync --extra dev --extra docs --upgrade
uvx pre-commit install
```

## Local Checks (Pre-commit)

```shell
git add .
uvx pre-commit autoupdate
uvx pre-commit run --all-files
```

## Build and Serve Docs

```shell
uv run mkdocs build --strict
uv run mkdocs serve
```
