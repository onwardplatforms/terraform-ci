# Shared pipelines for Terraform Continuous Integration

## Usage

### Features

* Formats and validates code
* Lints the code using TFLint
* Automatically adds documentation for the module

### Integration with Other Projects

In the remote project add this in `.github/workflows/github-ci.yml`:

```yaml
---
name: CI
on: [push]
jobs:
  ci:
    uses: onwardplatforms/terraform-ci/.github/workflows/terraform-ci.yaml@main
...
```

#### Notes

* Ref `main` can be changed for testing purpose