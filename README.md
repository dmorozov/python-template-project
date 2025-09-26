# Hello World Project

A modern Python "Hello World" project demonstrating best practices for Python development in 2025.

## Features

- 🏗️ Modern project structure with `src/` layout
- 📦 Dependency management with Poetry
- 🧹 Code quality tools (Ruff for linting and formatting, MyPy)
- 🧪 Testing with pytest and coverage reporting
- 🔧 Pre-commit hooks for code quality
- 💻 VSCode integration and settings
- 🐍 Virtual environment management

## Project Structure

```
hello-world-project/
├── src/
│   └── hello_world/
│       ├── __init__.py
│       └── main.py
├── tests/
│   ├── __init__.py
│   └── test_main.py
├── .vscode/
│   ├── settings.json
│   └── extensions.json
├── .pre-commit-config.yaml
├── .gitignore
├── pyproject.toml
└── README.md
```

## Setup and Installation

### Prerequisites

- Python 3.9 or higher
- Poetry (install from https://python-poetry.org/docs/#installation)

### Installation Steps

1. **Clone or create the project directory**
   ```bash
   mkdir hello-world-project
   cd hello-world-project
   ```

2. **Install Poetry** (if not already installed)
   ```bash
   curl -sSL https://install.python-poetry.org | python3 -
   ```

3. **Create the project files** (copy all the provided files into their respective locations)

4. **Install dependencies and create virtual environment**
   ```bash
   poetry install
   ```

5. **Activate the virtual environment**
   ```bash
   poetry env activate
   ```

6. **Install pre-commit hooks**
   ```bash
   poetry add --group dev pre-commit
   poetry run pre-commit install
   ```

## Usage

### Running the Application

```bash
# Using poetry
poetry run hello

# Or if virtual environment is activated
python src/hello_world/main.py

# Or using the installed script
hello
```

### Running Tests

```bash
# Run all tests
poetry run pytest

# Run tests with coverage
poetry run pytest --cov=src/hello_world

```

### Code Quality

```bash
# Format and lint code with Ruff
poetry run ruff format src tests
poetry run ruff check src tests

# Fix auto-fixable issues
poetry run ruff check --fix src tests

# Type check with MyPy
poetry run mypy src

# Run all quality checks
poetry run pre-commit run --all-files
```

## Development Workflow

1. **Make changes** to your code
2. **Run tests** to ensure functionality works
3. **Run code quality tools** or rely on pre-commit hooks
4. **Commit changes** (pre-commit hooks will run automatically)

## VSCode Setup

The project includes VSCode configuration for optimal development experience:

- **Recommended extensions** are specified in `.vscode/extensions.json`
- **Settings** are configured for Python development with proper formatting and linting
- **Testing integration** with pytest discovery
- **Type checking** with MyPy integration

### Recommended VSCode Extensions

- Python
- Ruff (combines formatting and linting)
- MyPy Type Checker

## Configuration

### Code Formatting & Linting
- **Ruff**: Fast Python linter and code formatter (replaces Black, isort, Flake8)
  - Line length 120
  - Comprehensive rule set including pycodestyle, pyflakes, pyupgrade, etc.
  - Auto-fixes many issues
- **MyPy**: Static type checking with strict mode

### Testing
- **pytest**: Test discovery and execution
- **Coverage**: Minimum 80% coverage required

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests and quality checks
5. Submit a pull request

## License

This project is open source and available under the MIT License.
