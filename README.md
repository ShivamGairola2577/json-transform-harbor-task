# JSON Age Filter – Harbor Task

## Overview

This Harbor task requires the agent to process a JSON file, filter users based on age, and write formatted output to a file.

Difficulty: Easy  
Category: data-processing

---

## Problem Description

An input JSON file is provided at:

/app/input.json

The file contains a list of users:

[
  {"name": "Alice", "age": 25},
  {"name": "Bob", "age": 17},
  {"name": "Charlie", "age": 30},
  {"name": "David", "age": 15}
]

---

## Requirements

The agent must:

1. Read `/app/input.json`
2. Filter users where `age >= 18`
3. Convert their names to uppercase
4. Sort the names alphabetically
5. Write the results to `/app/output.txt`

Each name must be written on a new line.

---

## Expected Output

For the provided input:

ALICE  
CHARLIE

---

## Validation

This task passes validation if:

- Oracle score = 1.0
- NOP score = 0.0
- Ruff linting passes
- All validation scripts succeed

---

## Notes

- Absolute paths must be used (`/app/...`)
- Output file must NOT be pre-created in Dockerfile
- The solution must compute the result dynamically
- The same canary GUID is used in Dockerfile, solve.sh, and tests
