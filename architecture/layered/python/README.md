# Python Layered Architecture Example

This is an example of a layered architecture in Python using FastAPI.

## Setup

This project uses `uv` for package management.

1.  **Create a virtual environment:**

    ```bash
    uv venv
    ```

2.  **Activate the virtual environment:**

    ```bash
    source .venv/bin/activate
    ```

3.  **Install dependencies:**

    ```bash
    uv pip install -e .[dev]
    ```

## Usage

To run the FastAPI application, first create a `src/main.py` file with the following content:

```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"Hello": "World"}
```

Then run the application with:

```bash
uvicorn src.main:app --reload
```
