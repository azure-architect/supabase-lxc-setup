# Supabase on Proxmox LXC Container

This repository contains configuration files for Supabase running in a Proxmox LXC container with ID 120.

## Container Specs
- Hostname: supabase
- Static IP: 192.168.0.120
- Resources: 4GB RAM, 2 CPU cores, 100GB storage

## Services
- Supabase Studio: http://192.168.0.120:3000
- Kong API Gateway: http://192.168.0.120:8000
- PostgreSQL: 192.168.0.120:5432

## Setup
1. Ensure Docker and Docker Compose are installed
2. Create `.env` file with required credentials (see .env.example)
3. Run `docker-compose up -d` to start all services

## Troubleshooting
If services are restarting or unhealthy:
- Check logs with `docker-compose logs service_name`
- Verify all environment variables are set correctly
- Ensure container has sufficient resources
