# Python

Personal workspace for **Python practice**, Jupyter tutorials, and a starter FastAPI stack.

Managed with [uv](https://docs.astral.sh/uv/). Requires **Python 3.14**.

## Setup

```bash
uv sync
```

This creates `.venv` and installs dependencies from `pyproject.toml` / `uv.lock`.

Alternative:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Select the `.venv` kernel in VS Code / Cursor when running notebooks (`ipykernel` is included).

## Project layout

```text
.
├── main.py                      # CLI entry: prints a hello message
├── pyproject.toml               # project metadata and dependencies
├── requirements.txt             # pip-friendly dependency list
├── uv.lock                      # locked uv versions
└── python/
    ├── 11_10_2026.ipynb         # session notebook (placeholder)
    └── tutorials/
        ├── functions.ipynb      # functions, lambda, map, filter, list comprehensions
        └── decorators_closures.ipynb  # function copy, closures, decorators
```

## Notebooks

| Notebook | Topics |
|---|---|
| [`python/tutorials/functions.ipynb`](python/tutorials/functions.ipynb) | Defining functions, `return` vs `print`, lambdas, `map`, `filter`, list comprehensions |
| [`python/tutorials/decorators_closures.ipynb`](python/tutorials/decorators_closures.ipynb) | Function copy, nested functions / closures, decorators |

## Run

```bash
uv run python main.py
```

FastAPI and Uvicorn are already in the environment for later API work:

```bash
uv run uvicorn main:app --reload
```

(`main.py` does not expose an `app` yet; add a FastAPI instance when you start that section.)

## Dependencies

- **python-dotenv** — load environment variables
- **fastapi** / **uvicorn** — HTTP APIs
- **numpy** / **pandas** — data work
- **ipykernel** — Jupyter in the editor
