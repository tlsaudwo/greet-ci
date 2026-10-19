# greet-ci

Run from the repository root with uv installed:

```bash
uv lock
uv run --locked python greet.py Hee
uv run --locked python greet.py
uv run --locked pytest -q greet.py
uv run --locked black --check greet.py
uv run --locked flake8 greet.py
uv run --locked mypy greet.py
uv build
```

CI runs on pushes to main and pull requests targeting main. It checks four
OS/Python combinations, formatting, lint, and types, then builds and saves
both distributions as the greet-dist artifact.
