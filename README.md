# Gakuya - Kenyan Weather Bot 🌤️

A Twitter bot that posts weather updates for Nairobi with a Kenyan twist! Gakuya combines weather information with trending topics in Kenya, adding humor and local references.

## Features

- 🌡️ Real-time weather updates for Nairobi
- 🔥 Integration with trending Kenyan topics
- 🤖 AI-generated witty posts using Grok AI
- 💬 Automatic replies to mentions
- 🏷️ Relevant hashtags and Kenyan references
- ⏰ Scheduled posts every 6 hours
- 🔄 Reply checks every 10 minutes

## Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/gakuya.git
cd gakuya
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Create a `.env` file with your API keys:
```
GROK_API_KEY=your_grok_api_key
OPENWEATHER_API_KEY=your_openweather_api_key
X_API_KEY=your_twitter_api_key
X_API_SECRET=your_twitter_api_secret
X_ACCESS_TOKEN=your_twitter_access_token
X_ACCESS_TOKEN_SECRET=your_twitter_access_token_secret
```

4. Run the bot:
```bash
python gakuya_bot.py
```

## Deployment on Render

1. Create a new Web Service on Render:
   - Go to [Render Dashboard](https://dashboard.render.com)
   - Click "New +" and select "Web Service"
   - Connect your GitHub repository

2. Configure the service:
   - Name: `gakuya-bot`
   - Environment: `Python 3`
   - Build Command: `pip install -r requirements.txt && python -m pip install --upgrade pip`
   - Start Command: `gunicorn gakuya_bot:app`
   - Plan: Free

3. Add Environment Variables:
   - Go to Environment section
   - Add all your API keys from `.env`:
     ```
     GROK_API_KEY
     OPENWEATHER_API_KEY
     X_API_KEY
     X_API_SECRET
     X_ACCESS_TOKEN
     X_ACCESS_TOKEN_SECRET
     PORT=10000
     ```

4. Deploy:
   - Click "Create Web Service"
   - Render will automatically deploy your bot

5. Monitor:
   - Check the "Logs" tab for bot activity
   - Use the "Events" tab to monitor deployments

## API Requirements

- [Grok AI](https://grok.ai) - For generating witty posts
- [OpenWeather](https://openweathermap.org) - For weather data
- [Twitter API](https://developer.twitter.com) - For posting and interactions

## Project Structure

- `gakuya_bot.py` - Main bot code
- `requirements.txt` - Python dependencies
- `.env` - Environment variables (not tracked in git)
- `gakuya.log` - Log file (not tracked in git)
- `last_tweet_id.json` - Last tweet tracking (not tracked in git)

## Contributing

Feel free to submit issues and enhancement requests!

## License

MIT License - feel free to use this project for your own weather bot! 