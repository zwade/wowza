# Wowza!

Wowza was a difficult web problem from PlaidCTF 2021. Players were tasked with using a search engine's site-management console to attack the search engine itself. The intended solution required exploiting a race condition in SQLite and a consistency bug in immutable.js. Unfortunately, a discrepency between `node-fetch` and the browser's built in `fetch` meant that the latter bug was not needed.

## Setup

First, build the docker containers for the problem

```bash
cd problem
yarn docker:all
```

Then, the easiest way to get started is to just run

```
docker-compose up -d
```
And navigate to `http://localhost:16284` and `http://localhost:16285`

Alternatively, the problem comes with a harness for running one instance per user. To set it up with the harness, run

```bash
cd ../harness
docker-compose build
docker-compose up -d
```

And navigate to `http://localhost:1064`
