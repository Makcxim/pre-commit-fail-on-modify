[![build status](https://github.com/pre-commit/pre-commit/actions/workflows/main.yml/badge.svg)](https://github.com/pre-commit/pre-commit/actions/workflows/main.yml)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/pre-commit/pre-commit/main.svg)](https://results.pre-commit.ci/latest/github/pre-commit/pre-commit/main)

## pre-commit

A framework for managing and maintaining multi-language pre-commit hooks.

For more information see: https://pre-commit.com/


Forked from https://github.com/pre-commit/pre-commit  

## Added  

fail on modify parameter to 'pre-commit run' command.  
That parameter control the behavior of the command when a hook modifies the files.  

## Example   

```yaml

repos:
  - repo: local
    hooks:
    - id: isort
      name: isort
      entry: isort
      language: python
      fail_on_modify: false
      types: ['python']
      additional_dependencies:
        - isort==5.10.1

```

## Made because 

Author of pre-commit library doesn't want to add this feature to the library.  
You can see:  

https://github.com/pre-commit/pre-commit/issues/747#issuecomment-386782080  
https://github.com/pre-commit/pre-commit/issues/532  
