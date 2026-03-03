# skill-woocommerce-stock-monitor

Monitor WooCommerce products for out-of-stock changes and send Telegram alerts. Tracks instock → outofstock transitions and alerts your team. Designed to run daily via cron.

## Usage

```bash
node scripts/stock-monitor.js
```

## Configuration

| Variable | Default | Description |
|---|---|---|
| `WOO_API_PATH` | `~/woo-api.json` | WooCommerce API credentials |
| `TELEGRAM_BOT_TOKEN` | — | Telegram bot token |
| `TELEGRAM_CHAT_ID` | — | Telegram group/chat ID for alerts |

### woo-api.json

```json
{
  "url": "https://yourstore.com",
  "consumerKey": "ck_...",
  "consumerSecret": "cs_..."
}
```

## Cron Setup (daily at 8 AM)

```bash
0 8 * * * cd /path/to/skill && node scripts/stock-monitor.js
```

## Requirements

- Node.js
- WooCommerce store with REST API enabled

## Part of the [Zero2Ai-hub](https://github.com/Zero2Ai-hub) skills ecosystem.
