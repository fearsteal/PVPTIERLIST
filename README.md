# Minecraft PvP Tier List

A responsive leaderboard platform for Minecraft PvP communities. It combines a browser-based leaderboard, a small Express API, JSON-backed tier data and Discord-bot integration.

## Highlights

- Overall and kit-specific leaderboards
- Player avatars, badges, tiers and points
- Responsive frontend built with Tailwind CSS
- Express API for reading and managing tier data
- Discord bot integration
- Community contribution and security documentation

## Architecture

```text
index.html       leaderboard UI
server.js        Express API
bot.js           Discord integration
tiers.json       local tier datastore
output.css       generated Tailwind styles
```

The frontend reads tier data from the API. Administrative integrations can add, update or remove player tiers through the backend.

## Getting started

```bash
git clone https://github.com/KayJss/PVPTIERLIST.git
cd PVPTIERLIST
npm install
node server.js
```

Serve the frontend with a static development server, for example:

```bash
npx serve .
```

## API

| Method | Endpoint | Purpose |
| --- | --- | --- |
| GET | `/api/tiers` | Return leaderboard data |
| POST | `/api/add-tier` | Add or update a player tier |
| POST | `/api/remove-tier` | Remove a player tier |

## Configuration

Update the server address and community-specific text in the frontend. Keep Discord credentials and API secrets outside source control and load them from environment variables in deployments.

## Security

Never commit bot tokens, API keys or production credentials. Review [SECURITY.md](SECURITY.md) before deploying the API publicly.

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) and the repository's pull-request template.

## License

MIT. See [LICENSE](LICENSE).

---

Built by [KayJss](https://github.com/KayJss).
