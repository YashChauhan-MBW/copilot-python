# Python Instructions

## Formatting (MANDATORY)
- Use black formatting
- Follow PEP8
- Keep code clean and readable

---

## Naming Rules
- Variables: snake_case
- Functions: snake_case
- Classes: PascalCase
- Constants: UPPER_CASE

Example:
```
user_input_path
load_data_file
DataProcessor
OUTPUT_DIR
```

---

## Input Handling (REQUIRED)
- Use argparse (no hardcoded files)

Example:
```python
import argparse
parser = argparse.ArgumentParser()
parser.add_argument("--input", required=True)
args = parser.parse_args()
```

---

## Output Handling (REQUIRED)
- Save files in `/output`
- Add timestamp to filename

Example:
```python
from datetime import datetime
from pathlib import Path

OUTPUT_DIR = Path("output")
OUTPUT_DIR.mkdir(exist_ok=True)
timestamp = datetime.now().strftime("%Y%m%d_%H%M%S")
file_path = OUTPUT_DIR / f"output_{timestamp}.csv"
```

---

## Code Reuse
- If logic is repeated → create a function
- Do NOT copy-paste logic

---

## Logging (Preferred)
Use logging instead of print:
```python
import logging
logging.basicConfig(level=logging.INFO)
```

---

## DO NOT DO
- No hardcoded paths
- No duplicate code
- No messy scripts
- No silent failures
