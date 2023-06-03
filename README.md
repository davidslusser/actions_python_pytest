# actions_python_pytest
A Github action for running unittests with pytest


<br/>

## How to use
In your .github/workflows directory, create a yaml file (such as main.yaml). Add a job for each desired workflow with the `uses` keyword. Use the `with` keyword to pass any desired variables.

Examples:

```
on: [push]

jobs:
  pytest:
    runs-on: ubuntu-latest
    name: "pytest"
    steps:
      - uses: davidslusser/actions_python_pytest@v1.0.0
```
<br/>

```
on: [push]

jobs:
  pytest:
    runs-on: ubuntu-latest
    name: "pytest"
    steps:
      - uses: davidslusser/actions_python_pytest@v1.0.0
        with:
          src: "src"
          options: "-v"
          pip_install_command: "pip install -e .[dev]"
          python_version: "3.9"
```


<br/>

## Inputs
  - **src:** source directory of code to check (defaults to "`.`")
  - **options:** optional flags/parameters used in pytest command
  - **pip_install_command:** pip install command (defaults to "`pip install pytest`")
   - **python_version:** version of python to run workflow with (defaults to "`3.x`")


<br/>
