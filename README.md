# ☁️ Weather Concierge Discord Bot

This Discord bot acts as your personal **weather concierge**, bringing real-time weather information directly to your server! Simply use the `!weather [city name]` command, and it will fetch temperature, humidity, wind speed, "feels like" temperature, and the current time for any location worldwide. Built with the `nextcord` API wrapper, it presents all this data in a sleek, visually appealing Discord embed, complete with a relevant weather icon. Empower your server members to stay informed about global conditions at a glance!

## ✨ Features

* **Effortless Access:** Get instant weather updates with the simple `!weather [city name]` command.
* **Comprehensive Data:** Provides detailed information, including:
    * Temperature (°C)
    * Humidity (%)
    * Wind Speed (KPH)
    * "Feels Like" Temperature (°C)
    * Current time in the specified location
    * Descriptive weather conditions (e.g., "Partly Cloudy," "Clear Sky")
* **Visual Appeal:** Displays weather data in a clean, intuitive Discord embed, enhanced by a dynamic weather icon.
* **Global Coverage:** Retrieve weather information for virtually any city around the world.

---

## 🚀 Installation & Setup

Get your Weather Concierge Bot up and running in a few simple steps.

### Prerequisites

Ensure you have the following installed and configured:

* **Python:** `v3.11.3` (or newer compatible versions)
* **Node.js:** `v20.13.1` (or newer, if used for project setup like dependency management, otherwise can be removed if strictly Python-only)
* **Discord Server:** Where you want to invite the bot.
* **Discord Bot Application & Token:** Create a bot in the [Discord Developer Portal](https://discord.com/developers/applications) and copy its unique token.
* **WeatherAPI Key:** Obtain a free API key from [WeatherAPI](https://www.weatherapi.com).

### Required Python Libraries

Install these using pip:

```bash
pip install nextcord==2.6.0 aiohttp==3.9.4
```

### Clone the Repository

First, get a copy of the bot's code to your local machine:

```bash
git clone https://github.com/<your-username>/weather-api-discord-bot.git
cd weather-api-discord-bot
```
*(Remember to replace `<your-username>` with your actual GitHub username.)*

---

## 🤖 Inviting the Bot to Your Server

Follow these steps carefully to set up your bot on Discord:

1.  **Create Your Application:** Go to the [Discord Developer Portal](https://discord.com/developers/applications) and click "New Application."
2.  **Create a Bot User:** Navigate to the **"Bot"** section on the left sidebar. Click "Add Bot" and then "Yes, do it!" Copy the **bot token** displayed there – this is highly sensitive and should be kept secret.
3.  **Configure OAuth2 Permissions:**
    * Go to the **"OAuth2"** section on the left sidebar, then click **"URL Generator"** (or just "OAuth2" and then "Add a Scopes").
    * Under **"Scopes"**, select `bot`.
    * Under **"Bot Permissions"**, grant the following:
        * `Send Messages`
        * `Embed Links`
4.  **Generate Invite Link:** Copy the generated URL at the bottom of the "OAuth2 URL Generator" page. Paste this URL into your browser, select your desired Discord server, and authorize the bot to join.

---

## ⚙️ Configuration & Run

### Bot Intents (Important!)

Before running the bot, you **must** enable the following **Privileged Gateway Intents** under the **"Bot"** section in the [Discord Developer Portal](https://discord.com/developers/applications):

* **PRESENCE INTENT**
* **SERVER MEMBERS INTENT**
* **MESSAGE CONTENT INTENT**

These are necessary for the bot to read messages and function correctly.

### Setup `config.py`

In the root of your cloned project, you'll find a `config.py` file. Open it and replace the placeholder values with your actual tokens:

```python
# config.py
DISCORD_BOT_TOKEN = "YOUR_DISCORD_BOT_TOKEN_HERE"
WEATHER_API_KEY = "YOUR_WEATHER_API_KEY_HERE"
```

### Running the Bot

Once `config.py` is updated and the required Python libraries are installed, you're ready to launch the bot!

1.  Ensure the bot is present in your desired Discord server.
2.  From your terminal, inside the `weather-api-discord-bot` directory, run the main bot file:

    ```bash
    python weather.py
    ```

    The bot should come online and appear active in your Discord server!

---
