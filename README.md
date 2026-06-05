# Final_Project_NLP
Tokopedia review-rating consistency detector.

## Minimal backend

This project uses OpenRouter for inference. There is no training notebook required.

### Install

```bash
npm install
```

### Configure

Copy `.env.example` to `.env` and add your OpenRouter API key.

### Run

```bash
npm run dev
```

### Endpoints

- `GET /api-docs`
- `GET /models`
- `GET /health`
- `POST /analyze`
- `POST /analyze-batch`
- `POST /analyze-bulk`

## Docker

Build the image:

```bash
docker build -t your-dockerhub-user/tokopedia-review-consistency-detector:latest .
```

Push it to Docker Hub:

```bash
docker push your-dockerhub-user/tokopedia-review-consistency-detector:latest
```

Run it with Docker Compose:

```powershell
$env:DOCKER_IMAGE="your-dockerhub-user/tokopedia-review-consistency-detector:latest"
docker compose up -d
```

The container reads runtime variables from `.env`, so each person can keep their own OpenRouter key locally.
