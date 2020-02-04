# Continue Watching API

Example of a simple implementation to build a continue watching api on top of Redis

## Requirements

- nodejs v10+
- redis

## Usage
- `git clone git@github.com:Eyevinn/continue-watching-api.git`
- `cd continue-watching-api`
- `npm install`
- Start Redis locally or insert the needed keys into the .env file
- `npm start` to run the server

## Endpoints

- POST `/position/:userId/:assetId/:position` where position is in seconds
- GET `/position/:userId/:assetId` to get position on a given asset
- GET `/position/:userId` to get all positions for a specific user, newest first.

## Environment variables

- `NODE_ENV` if set to `development` there will be some logging made into the console
- `REDIS_URL` if not local
- `REDIS_PORT` if not default (6379)
- `REDIS_AUTH`