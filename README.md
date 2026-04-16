# CsYBot

CsYBot is a shard-enabled Discord bot and web panel project that provides advanced moderation and panel features for Discord servers. This repository includes the bot core, web panel, commands, events, and a MongoDB-based data layer.

## Features
- Shard-enabled Discord bot infrastructure
- Web panel (Express + EJS)
- Discord login with OAuth2
- Top.gg vote tracking and webhook notifications
- Uptime monitoring and API integrations
- Multi-language support via language files

## Technology
- Node.js
- discord.js v13
- Express, EJS
- MongoDB (Mongoose)
- Passport (Discord OAuth)

## Installation
1. Clone the repository.
2. Install dependencies:

```bash
npm install
```

3. Set environment variables (for example, `.env`):

```bash
# required
PORT=3000
mongodb=mongodb+srv://<user>:<pass>@<cluster>/<db>
token=DISCORD_BOT_TOKEN
secret=DISCORD_OAUTH_CLIENT_SECRET

# optional / integrations
TOPGG_TOKEN=
TOPGG_PASS=
RECAPTCHA_SECRET=
RECAPTCHA_PUBLIC=
```

4. Update the placeholder fields in `config.js` with your own values.

## Run
```bash
npm start
```

This command starts shard management through `shard.js`. The web panel starts on shard 0.

## Directory Structure (short)
- `commands/` Discord commands
- `events/` Discord event handlers
- `functions/` shared functions/helpers
- `views/` web panel and API layer
- `databases/` MongoDB models and data access

## Security Notes
- Do not commit real token/secret values to the repository. Keep `config.js` and `.env` values private.
- There is a hardcoded session secret in `views/libs/global.js`. It is recommended to move it to an environment variable.

## License
MIT
