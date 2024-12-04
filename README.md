# UNOFFICIAL Zoneminder Docker Compose + SSL + Pushover + Event Server
This is based on https://github.com/zoneminder-containers/eventserver-base . I made this version because I needed to:
- use the host mode for networking (I have some cameras that use RTCP over UDP and it has some problem on the dockerized network interface)
- use SSL
- use Pushover as notification service
- Mount externally /zm/data in order to be able to sync event video files to external cloud services
- update Zoneminder more frequently in a safer way

## Setup
1. Set up an account with Pushover
2. Set up secrets in zm/config/secrets.ini
3. Set up a SSL certificate and put certificates in zm/config/ssl
4. Run docker compose build
5. Run docker compose up -d
