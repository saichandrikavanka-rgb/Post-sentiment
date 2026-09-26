# InfluenceIQ / ScreenIQ

Influencer intelligence and post-sentiment analysis platform for YouTube and authorized Instagram data.

## Step 1 - Backend + Database

### Start MariaDB
```bash
docker compose up -d mariadb
```

### Backend setup
```bash
cd backend
python -m venv .venv
# Windows
.venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload
```

Health endpoint:
`GET http://127.0.0.1:8000/health`

Swagger:
`http://127.0.0.1:8000/docs`

The database schema is in `database/schema.sql` and follows the normalized cross-platform model for platforms, influencers, accounts, posts, metrics, comments, sentiment, aspects, historical metrics, collection jobs, analysis runs, and agent runs.
