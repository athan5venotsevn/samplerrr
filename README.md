# Musical Waddle

A Telegram bot that can stream Telegram files to users over HTTP.

## Setup
Install dependencies (see [requirements.txt](/requirements.txt)), configure
environment variables (see below) and run with `python3 -m tgfilestream`.

A reverse proxy is recommended to add TLS. When using a reverse proxy, keep
`HOST` as-is, but add the publicly accessible URL to `PUBLIC_URL`. The URL
should include the protocol, e.g. `https://example.com`.

### You can also tap the Deploy To Heroku button below to deploy straight to Heroku!

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new/template?template=https%3A%2F%2Fgithub.com%2Fathan5venotsevn%2Fmusical-waddle&envs=TG_API_ID%2CTG_API_HASH%2CBOT_TOKEN%2CHOST%2CPUBLIC_URL&TG_API_IDDesc=Your+Telegram+API+ID.&TG_API_HASHDesc=Your+Telegram+API+hash.&BOT_TOKENDesc=from+t.me%2Fbotfather+itself&HOSTDesc=%28defaults+to+0.0.0.0%29+-+The+port+to+listen+at.&PUBLIC_URLDesc=Railway+app+URL&HOSTDefault=0.0.0.0)

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/TGExplore/musical-waddle/tree/master)

### Environment variables
* `TG_API_ID` (required) - Your Telegram API ID.
* `TG_API_HASH` (required) - Your Telegram API hash.
* `TG_SESSION_NAME` (defaults to `tgfilestream`) - The name of the Telethon session file to use.
* `PORT` (defaults to `8080`) - The port to listen at.
* `HOST` (defaults to `localhost`) - The host to listen at.
* `PUBLIC_URL` (defaults to `http://localhost:8080`) - The prefix for links that the bot gives.
* `TRUST_FORWARD_HEADERS` (defaults to false) - Whether or not to trust X-Forwarded-For headers when logging requests.
* `DEBUG` (defaults to false) - Whether or not to enable extra prints.
* `LOG_CONFIG` - Path to a Python basic log config. Overrides `DEBUG`.
* `REQUEST_LIMIT` (default 5) - The maximum number of requests a single IP can have active at a time.
* `CONNECTION_LIMIT` (default 20) - The maximum number of connections to a single Telegram datacenter.

## Thanks

Thanks to [Tulir Asokan](https://github.com/tulir "Tulir Asokan") for his [TgFileStream](https://github.com/tulir/tgfilestream "TgFileStream") Bot.
