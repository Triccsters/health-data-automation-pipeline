# health-data-automation-pipeline
An end-to-end automated ETL pipeline orchestrating Tasker, Python, and Zapier for real-time health metric analysis.
#  Automated Health Data Pipeline
### Tasker | Python | Zapier | Gemini AI

## Project Overview
This project is a custom-engineered ETL (Extract, Transform, Load) pipeline designed to eliminate manual health tracking. It orchestrates a mobile trigger, a local Python processing engine, and cloud-based AI to turn raw biometrics into actionable daily insights.

## System Architecture
* **Trigger (Tasker):** Captures mobile events (e.g., gym check-ins) and acts as a metronome to ping the local server.
* **Processing (Python):** A custom script running on a Windows desktop that extracts data from Health Connect/Oura, sanitizes SI units, and handles "Upsert" logic to prevent duplicate entries in a Google Sheet database.
* **Orchestration (Zapier):** Monitors the database, routes specific metrics to specialized Gemini AI "Coaches," and appends a summarized brief to an Evernote Daily Note.

## Technical Competencies
* **API Integration:** Managing RESTful webhooks and handling API rate limits (Evernote 429 error mitigation).
* **Infrastructure:** Deploying background processes on Windows using `pythonw.exe`.
* **Data Sanitization:** Converting raw JSON payloads into structured, human-readable data.
