# twspace-crawler

## Description

Script to crawl & download Twitter Spaces.

## Requirements

- [Node 14](https://nodejs.org/)
- [ffmpeg](https://www.ffmpeg.org/)

## Installation

```
npm install
```

```
npm run build
```


## Usage

```
node ./dist/index.js --user nakiriayame
```

```
node ./dist/index.js --config ./config.json
```

## Options

```
  -h, --help                Display help
  -d, --debug               Show debug logs

  --config <CONFIG_PATH>    Load config file (Check config.json)
  --user <USER>             Watch & download live Spaces from users, separate by comma (,)
  --id <SPACE_ID>           Watch & download live Space with id
  --force                   Force download Space when using with --id
  --url <PLAYLIST_URL>      Download Space using playlist url

  --notification            Show notification about new live Space
```
## Commands

```
  cc download|d <SPACE_ID> <TOKEN>  Download Space captions
  cc extract|e <FILE>               Extract Space captions
```

## Advance Usage

- To watch multiple users, it is better to use [Twitter API](https://developer.twitter.com/en/docs/twitter-api/spaces/overview)
    1. Clone `.env.example` and rename to `.env`
    2. Get `Bearer Token` ([Docs](https://developer.twitter.com/en/docs/twitter-api/getting-started/getting-access-to-the-twitter-api))
    3. Set `TWITTER_AUTHORIZATION` value to `Bearer Token` value
       ```
       TWITTER_AUTHORIZATION = "Bearer AAAAAAAAAAAAAAAAAAAAANRILgAAAAAAnNwIzUejRCOuH5E6I8xnZz4puTs..."
       ```
