# GamesPlay Backend (Dockerized)

Minimal setup to run the GamesPlay Django backend with Postgres using Docker Compose.

Steps to run:

1. **Clone the repository**:

```bash
   git clone git@github.com:filkin1912/gamesplay-docker.git
   cd gamesplay-docker
```   

2. **Pull the backend image from Docker Hub**:

```bash
   docker pull filk1912/gamesplay-backend
```

3. **Start the stack**:

```bash
   docker-compose up -d
```

4. **Initialize Django**:

```bash
   docker-compose exec backend python manage.py migrate
   docker-compose exec backend python manage.py createsuperuser
   docker-compose exec backend python manage.py collectstatic --noinput
```

5. **Seed demo games (after logging in with your superuser)**:
   http://localhost:8001/seed_games

6. **Access the web app**:
    - App: http://127.0.0.1:8001
    - Admin: http://127.0.0.1:8001/admin (log in with your superuser credentials)
