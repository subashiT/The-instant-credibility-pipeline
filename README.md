# Todo API — CI/CD Demo

![CI](https://github.com/YOUR_USERNAME/todo-api/actions/workflows/ci-cd.yml/badge.svg)

**Live demo:** https://your-app.railway.app/health

This repo demonstrates a complete automated delivery pipeline. 
Every code change goes through quality checks and ships to 
production automatically — no manual steps.

## How the pipeline works

### 1. Lint (code quality check)
Flake8 checks that all Python code follows consistent style rules.
This catches obvious errors and enforces readability before 
anything else runs.

### 2. Test (automated verification)
Pytest runs unit tests against the API endpoints. If any test 
fails, the pipeline stops here — nothing broken ever reaches 
production.

### 3. Docker build (packaging)
The app is packaged into a Docker container — a self-contained 
unit that includes the app and every dependency it needs. 
It will run identically on any server in the world.

### 4. Push to Docker Hub (artifact storage)
The container image is pushed to Docker Hub, a public registry. 
This is the "built artifact" — the exact version of the app 
that will be deployed.

### 5. Deploy (go live)
Railway pulls the new image and replaces the running container. 
Zero-downtime deployment. The live URL is updated within seconds.

## Running locally
...
