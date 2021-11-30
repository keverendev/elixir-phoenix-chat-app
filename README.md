# A simple chat app using Elixir/Phoenix and WebSockets


## Setup

Installing Kafka:

```
$ brew install kafka
$ brew services start zookeeper
$ brew services start kafka
```

Zookeeper is running on port 2181, Kafka on port 9092.

### Web Application

To start your Phoenix app:

  * Install dependencies with `mix deps.get`
  * Create and migrate your database with `mix ecto.create && mix ecto.migrate`
  * Install Node.js dependencies with `npm install`
  * Start Phoenix endpoint with `mix phoenix.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

### Kafka Worker

There is a separate process that streams messages from Kafka and writes them to Postgres.

```
$ mix run lib/ingest/writer.exs
```

