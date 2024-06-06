# Docker Compose Setup for Nginx Proxy, Docker Gen, ACME Companion, Excalidraw, and Doom
This repository provides a Docker Compose setup to run an Nginx reverse proxy, automatically update Nginx configurations using Docker Gen, manage SSL certificates using ACME Companion, and host two services: Excalidraw and Doom in Docker.

## Prerequisites
- Docker
- Docker Compose

## Services
1. Nginx Proxy: Acts as a reverse proxy for all incoming traffic.
2. Docker Gen: Dynamically generates Nginx configuration files.
3. ACME Companion: Handles SSL certificate generation and renewal.
4. Excalidraw: A collaborative whiteboard tool.
5. Doom: The classic Doom game hosted in a Docker container.

## Configuration
docker-compose.yml

## Usage

  1. Clone the repository:
  
    git clone https://github.com/luis198755/Excalidraw-Doom.git
  
  2. Start the services:
  
    docker-compose up -d
  
  3. Access the services:
  
    - Excalidraw: http://draw.ejemplo.com
    - Doom: http://doom.ejemplo.com

## Environment Variables

  - DEFAULT_EMAIL: Email address for Let's Encrypt notifications.
  - VIRTUAL_HOST: Domain for the service.
  - VIRTUAL_PORT: Port the service listens on.
  - LETSENCRYPT_HOST: Domain for SSL certificate.
  - LETSENCRYPT_MAIL: Email for SSL certificate registration.
  - REACT_APP_BACKEND_V1_GET_URL, REACT_APP_BACKEND_V2_GET_URL, REACT_APP_BACKEND_V2_POST_URL: Backend URLs for Excalidraw.

## Volumes

  - conf: Nginx configuration files.
  - vhost: Nginx virtual host files.
  - html: HTML files served by Nginx.
  - certs: SSL certificates.
  - acme: ACME challenge data.
