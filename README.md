## 👋 Welcome to owncloud 🚀

Self-hosted owncloud application

## 📋 Description

Self-hosted owncloud application

## 🚀 Services

- **app**: owncloud/server:latest

### Infrastructure Components

- **db**: Mariadb database
- **redis**: Redis database


## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/owncloud/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/owncloud" ~/.local/srv/docker/owncloud
cd ~/.local/srv/docker/owncloud
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install owncloud
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
DB_CREATE_DATABASE_NAME=owncloud
DB_USER_NAME=owncloud
DB_USER_PASS=changeme_db_password
APP_ADMIN_USER=admin
APP_ADMIN_PASS=changeme_admin_password
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:60236

## 📂 Volumes

- `./volumes/data/owncloud` - Data storage
- `./volumes/data/db/mariadb/owncloud` - Data storage
- `./volumes/data/db/redis/owncloud` - Data storage

## 🔐 Security

- Change all default passwords before deploying to production
- Use strong secrets for all authentication tokens
- Configure HTTPS using a reverse proxy (nginx, traefik, caddy)
- Regularly update Docker images for security patches
- Backup your data regularly

## 🔍 Logging

```shell
docker compose logs -f app
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
