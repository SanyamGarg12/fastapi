# Contributing to FastAPI

Thank you for your interest in contributing to FastAPI! 🎉

For detailed guidelines, please read the [Development - Contributing](https://fastapi.tiangolo.com/contributing/) documentation.

## Local Development Setup

### Prerequisites

- **Python 3.10+** (3.11 recommended, as pinned in `.python-version`)
- **[uv](https://docs.astral.sh/uv/)** — used as the package manager

---

### Linux / macOS

#### 1. Fork & Clone

```bash
git clone https://github.com/<your-username>/fastapi.git
cd fastapi
```

#### 2. Install uv (if not already installed)

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
source $HOME/.local/bin/env   # or restart your shell
```

#### 3. Install Dependencies

```bash
uv sync --group tests
```

#### 4. Run the Tests

```bash
uv run pytest tests -q -n auto
```

#### 5. Linting & Type Checking

```bash
uv run ruff check fastapi/
uv run ruff format fastapi/
uv run mypy fastapi/
```

#### 6. Create a Branch & Push

```bash
git checkout -b my-feature-branch
# ... make your changes ...
git add .
git commit -m "Describe your change"
git push origin my-feature-branch
```

Then open a Pull Request on GitHub.

---

### Windows

#### 1. Fork & Clone

```powershell
git clone https://github.com/<your-username>/fastapi.git
cd fastapi
```

#### 2. Install uv (if not already installed)

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

After installation, restart your terminal so `uv` is available on your PATH.

#### 3. Install Dependencies

```powershell
uv sync --group tests
```

#### 4. Run the Tests

```powershell
uv run pytest tests -q -n auto
```

#### 5. Linting & Type Checking

```powershell
uv run ruff check fastapi/
uv run ruff format fastapi/
uv run mypy fastapi/
```

#### 6. Create a Branch & Push

```powershell
git checkout -b my-feature-branch
# ... make your changes ...
git add .
git commit -m "Describe your change"
git push origin my-feature-branch
```

Then open a Pull Request on GitHub.

---

## Useful Tips

- Run a **specific test file**: `uv run pytest tests/test_your_file.py -v`
- **Skip the CLI test** (known pre-existing failure): `uv run pytest tests -q -n auto --ignore=tests/test_fastapi_cli.py`
- The project uses **ruff** for linting/formatting and **mypy** for type checking — make sure both pass before submitting your PR.
