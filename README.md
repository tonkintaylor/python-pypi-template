# Python PyPI Package Template

A minimal template for creating Python packages with a simple "Hello World" example.

## Quick Start

### 1. Use this template

Click the "Use this template" button on GitHub to create your own repository:

### 2. Install dependencies

```bash
# Run the development setup script
.\tasks\dev_sync.ps1
```

### 3. Customize the package

#### Rename the package

1. Rename directories:
   ```bash
   mv src/whitelable src/YOUR_PACKAGE_NAME
   mv tests/whitelable tests/YOUR_PACKAGE_NAME
   ```

2. Update `pyproject.toml`:
   - Change `name = "whitelable"` to `name = "YOUR_PACKAGE_NAME"`
   - Update author information
   - Update repository URLs

3. Update import statements in your code from `whitelable` to `YOUR_PACKAGE_NAME`

### 4. Test your setup

```bash
# Run tests
pytest

# Run the hello world example
python -c "from YOUR_PACKAGE_NAME.functions.hello_world import hello_world; print(hello_world('World'))"
```

## Project Structure

```
├── src/YOUR_PACKAGE_NAME/     # Main package
│   ├── functions/            # Your functions
│   └── __init__.py
├── tests/YOUR_PACKAGE_NAME/  # Tests
├── pyproject.toml           # Package configuration
└── README.md                # This file
```

## Usage Example

```python
from YOUR_PACKAGE_NAME.functions.hello_world import hello_world

# Basic usage
result = hello_world()
print(result)  # "Hello, World!"

# With custom name
result = hello_world("Alice")
print(result)  # "Hello, Alice!"
```

## Next Steps

1. Replace the hello_world function with your own code
2. Add your functions to `src/YOUR_PACKAGE_NAME/functions/`
3. Write tests in `tests/YOUR_PACKAGE_NAME/`
4. Update `pyproject.toml` with your package details
5. Build and publish: `python -m build && twine upload dist/*`

## License

MIT License
