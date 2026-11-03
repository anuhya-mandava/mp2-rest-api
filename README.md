# MP2: Data Processing REST API

This FastAPI application lets a client upload a CSV file, store it in memory, retrieve its rows, and clean it using the reusable data pipeline from MP1. `POST /upload` stores a CSV and returns its metadata, `GET /datasets/{id}` returns up to `limit` rows, and `POST /datasets/{id}/process` validates and processes a stored dataset using a JSON configuration, returning a cleaning report. `GET /health` reports the API status. Every request is logged with a unique request ID, status code, and duration, and the core workflow is covered by pytest tests.

Run the API with `python -m uvicorn main:app --reload` and open `/docs`. Run the tests with `python -m pytest tests -v`.