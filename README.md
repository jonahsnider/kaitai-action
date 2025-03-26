# Setup Kaitai Action

A GitHub Action to setup the Kaitai Struct compiler.

## Usage

```yml
name: CI

on: [push, pull_request]

jobs:
  ksc:
    name: Run kaitai-struct-compiler

    runs-on: ubuntu-latest

    steps:
      - name: Checkout Git repository
        uses: actions/checkout@v4
      - name: Setup Kaitai Struct compiler
        uses: jonahsnider/kaitai-action@v1.0.1
      - name: Run kaitai-struct-compiler
        run: kaitai-struct-compiler --version
```
