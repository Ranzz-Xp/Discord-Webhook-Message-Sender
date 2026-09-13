# Discord Webhook Sender

A single-file HTML tool for sending custom messages to a Discord webhook repeatedly, with configurable delay, rate-limit handling, and a stop button. Runs entirely in the browser — no server, no build step, no dependencies.

## Live Demo

Once GitHub Pages is enabled for this repository, the tool will be available at:
https://ranzz-xp.github.io/Discord-Webhook-Message-Sender/

## Features

- Single HTML file — just open it in a browser.
- Send a custom message any number of times.
- Adjustable delay between messages (in milliseconds).
- Optional override for webhook username and avatar.
- Automatic handling of Discord `429` rate limits (respects `retry_after`).
- Live log with timestamps and a progress bar.
- Stop button to abort mid-run.
- Validates webhook URL format before starting.
- No data leaves your browser except the requests sent directly to Discord.

## Quick Start

1. Download or clone this repository.
2. Open `index.html` in any modern browser (Chrome, Firefox, Edge, etc.).
3. Paste your Discord webhook URL into the **Webhook URL** field.
4. Type the message you want to send.
5. Set the number of times to send and the delay between sends.
6. (Optional) Override the username and avatar.
7. Click **Start**.

The log panel will show each attempt, any rate-limit warnings, and errors.

## Configuration

| Field | Description | Default |
|-------|-------------|---------|
| Webhook URL | Your Discord webhook endpoint. Must match the expected format. | – |
| Message | The text content to send. | – |
| How many times | Number of messages to send. | 10 |
| Delay between (ms) | Milliseconds to wait between successful sends. | 1000 |
| Override username | Optional display name for the webhook. | (webhook default)  |
| Avatar URL | Optional avatar image URL. | (webhook default) |
