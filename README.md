# YouTube Video Alert & Tracker (n8n)

I built this simple n8n automation to keep track of new uploads from my favorite YouTube channels without needing a YouTube API key. Whenever a new video goes live, it automatically saves the details to a Google Sheet and sends me an email alert.

## How it works
- Checks for updates: An RSS Feed Trigger checks the channel's XML feed every hour.
- Saves a record: When a new video pops up, Google Sheets logs the Title, Link, and Published Date as a new row so nothing gets overwritten.
- Sends an alert: Gmail immediately sends me an email with the video title and a direct link to watch it.

## Setup
1. Download the .json file from this repo and import it into your n8n dashboard.
2. Open the RSS Feed Trigger node and swap in your target YouTube channel's channel_id.
3. Connect your own Google Sheets and Gmail accounts in the credentials.
4. Hit Save and toggle the workflow to Active.
