# nbdime-action

Can't use https://www.reviewnb.com/ ? This may be the next best thing.

Example:

`.github/workflows/nbdime-git-diff.yml`:

```
name: nbdime-git-diff
on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
      with:
        fetch-depth: 0
    - name: Set up Python 3.9
      uses: actions/setup-python@v3
      with:
        python-version: "3.9.13"
    - name: nbdime-git-diff
      uses: raybellwaves/nbdime-git-diff@0.0.4
```
