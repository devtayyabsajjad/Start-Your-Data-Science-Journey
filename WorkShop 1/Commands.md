# Conda Environment Management

## Listing Existing Environments
```bash
conda env list
```
This command shows all currently available Conda environments on your system.

## Creating a New Conda Environment
```bash
# Create a new environment with a specific name
conda create --name workshop_no_1

# Activate the newly created environment
conda activate workshop_no_1

# Install a specific Python version
conda install python=3.11

# Install IPython kernel (for Jupyter notebook support)
conda install ipykernel
```

## Python Virtual Environment Alternative (venv)
```bash
# Create a virtual environment
python -m venv workshop_no_1

# Activate the environment
# On Windows
workshop_no_1\Scripts\activate

# On macOS/Linux
source workshop_no_1/bin/activate

# Deactivate the environment
deactivate
```

## Key Differences Between Conda and venv
- Conda: 
  - Manages packages and environments
  - Works across multiple programming languages
  - More robust package management
  - Easier to handle complex dependencies

- venv:
  - Python-specific virtual environment
  - Lighter weight
  - Part of Python standard library
  - Simpler to use for pure Python projects

## Best Practices
1. Always create a new environment for each project
2. Specify Python version when creating environments
3. Use `requirements.txt` or `environment.yml` to replicate environments
4. Deactivate environments when not in use

## Useful Conda Commands
```bash
# Remove an environment
conda env remove --name workshop_no_1

# Export environment dependencies
conda env export > environment.yml

# Create environment from yml file
conda env create -f environment.yml
```

💡 Pro Tip: Choose the environment management tool that best fits your project's complexity and requirements