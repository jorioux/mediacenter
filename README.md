# Docker Media Center
docker-compose file for a complete media center

## Usage
On the Docker Host, the media storage must be in `/mnt/data`

#### 1. Create the folders
* `/mnt/data/medias` (movies and tv shows)
* `/mnt/data/downloads` (deluge downloads
* `/mnt/data/transcode` (plex transcoding)
* `/mnt/data/plex` (plex config)
* `/mnt/data/radarr` (radarr config)
* `/mnt/data/sonarr` (sonarr config)
* `/mnt/data/jackett` (jackett config)

You can backup the config folders once in a while.

#### 2. Create the dotenv file
Copy `.env.example` to `.env` and fill the variables.

#### 3. Create the persistent volumes
`docker volume create plexconfig`
`docker volume create delugeconfig`

#### 3. Launch it
`docker-compose up -d`
