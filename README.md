# RihannaUI

A beautiful UI for [Rihanna](https://github.com/samphilipd/rihanna).

You can run it from Docker Hub - [samphilipd/rihanna_ui](https://hub.docker.com/r/samphilipd/rihanna_ui/).

![Rihanna UI screenshot](docs/rihanna_ui_screenshot.png)

## Building docker image

You shouldn't need to do this since you can just download it from dockerhub, but here is an example of how to build your own docker image for production:

`docker build . --build-arg MIX_ENV=prod -t rihanna_ui:latest`

## Configuration

You must pass in environment configuration so that RihannaUI can connect
to the database with your `rihanna_jobs` table, like so:

`DB_USERNAME=postgres DB_PASSWORD=postgres DB_DATABASE=rihanna_db DB_HOSTNAME=localhost DB_PORT=5432 mix phx.server`

## Development

To start your Phoenix server:

  * Install dependencies with `mix deps.get`
  * Install Node.js dependencies with `cd assets && npm install`
  * Start Phoenix endpoint with `mix phx.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.
