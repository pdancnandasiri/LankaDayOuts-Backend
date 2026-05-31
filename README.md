# LankaDayOuts-Backend

Simple backend for LankaDayOuts (FastAPI service).

## Tech Stack

- **Language:** Python 3.9+
- **Web framework:** FastAPI
- **ASGI server:** Uvicorn
- **ORM / DB:** SQLAlchemy (db/session.py)
- **Validation:** Pydantic

## Folder structure

Project layout (important files):

- [app/main.py](app/main.py#L1) — FastAPI application entry
- [app/api/health.py](app/api/health.py#L1) — health check endpoint
- [app/api/deps.py](app/api/deps.py#L1) — dependency helpers
- [core/config.py](core/config.py#L1) — configuration
- [db/session.py](db/session.py#L1) — database session setup

Top-level layout:

```
.
├── app/
│   ├── main.py
│   └── api/
│       ├── deps.py
│       └── health.py
├── core/
│   └── config.py
├── db/
│   └── session.py
├── 2.0
├── LICENSE
```

## Setup

1. Create and activate a virtual environment:
   - Windows (PowerShell):

     ```powershell
     python -m venv .venv
     .\.venv\Scripts\Activate.ps1
     ```

   - Windows (cmd):

     ```cmd
     python -m venv .venv
     .\.venv\Scripts\activate
     ```

2. Install dependencies (create `requirements.txt` if not present):

   ```bash
   pip install -r requirements.txt
   ```

Common dependencies to include in `requirements.txt`:

- fastapi
- uvicorn[standard]
- sqlalchemy

## Run

Start the app with Uvicorn (development mode):

```bash
uvicorn app.main:app --reload --host 127.0.0.1 --port 8000
```

Open interactive docs at: http://127.0.0.1:8000/docs

## Notes

- Adjust environment variables and database URL via [core/config.py](core/config.py#L1).
- If you add migrations, include Alembic or your chosen tool.

## Contributing

Feel free to open issues or submit PRs. Keep changes small and document any new dependencies.
