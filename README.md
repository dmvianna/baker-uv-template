# [uv](docs.astral.sh/uv) template for [Baker](https://github.com/aliev/baker)

## Overview

This template creates a project scaffolding for [Python](python.org)
using [pytest](pytest.org) and
[pytest-watcher](github.com/olzhasar/pytest-watcher) as its test
runner.

It also includes common development tools such as `pyright`,
`jupyter` and `ruff`.

## Dependencies

- [Baker](https://github.com/aliev/baker): A command-line tool that
  helps you quickly scaffold new projects. It is implemented in
  [Rust](www.rust-lang.org), but is language-agnostic. You can create
  projects and write scripts to help scaffolding in any language. The
  main templating engine uses [Mini Jinja](docs.rs/minijinja).

- [git](git-scm.com): This template creates an empty **git** in the
  project directory. It also defaults the project author and email to
  the ones defined in the global **git** config.

- [bash](www.gnu.org/software/bash): The hooks in the present template
  are written as **Bash** scripts.

- [jq](jqlang.org): We use **jq** to read variables from the template
  engine context to our hooks.

- [uv](docs.astral.sh/uv): This template will create **Python**
  project scaffolding with the **uv** package manager. **uv** is
  implemented in [Rust](www.rust-lang.org).

# Development tools

- [Jupyter](jupyter.org) is an interactive **Python** shell. Its
  notebook version is implemented as a web server, which makes it
  possible to present images and many other desirable features. You
  can run **Jupyter notebook** with `uv run jupyter notebook`.

- [pytest-watcher](github.com/olzhasar/pytest-watcher) is a test
  runner that runs tests each time a `*.py` file is changed in the
  project. You can configure it to run in response to other file
  extensions too. Just add something like

  ```toml
  [tool.pytest-watcher]
  patterns = ["*.py", "*.csv", "*.json"]
  ```

  to `pyproject.toml` and it will run the tests when you change
  **JSON** or **CSV** files too.

  You can run **pytest-watcher** with `uv run ptw .`.
