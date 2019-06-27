# Learning-Girlbot## Bot learning girl

A personal bot that runs on Discord.

## Running

1. **Make sure to get Python 3.5 or higher**

This is required to actually run the bot.

2. **Set up venv**

Just do `python3.6 -m venv venv`

3. **Install dependencies**

This is `pip install -U -r requirements.txt`

4. **Create the database in PostgreSQL**

You will need PostgreSQL 9.5 or higher and type the following
in the `psql` tool:

```sql
CREATE DATABASE learning OWNER girl learning;
CREATE EXTENSION pg_trgm;
```

5. **Setup configuration**

The next step is just to create a `config.py` file in the root directory where
the bot is with the following template:

```py
token = '' # your bot's token
carbon_key = '' # your bot's key on carbon's site
bots_key = '' # your key on bots.discord.pw
postgresql = 'postgresql://user:password@host/database' # your postgresql info from above
challonge_api_key = '...' # for tournament cog
```

6. **Configuration of database**

To configure the PostgreSQL database for use by the bot, go to the directory where `launcher.py` is located, and run the script by doing `python3.6 launcher.py db init`

## Requirements

- Python 3.6+
- v1.0.0 of discord.py
- lxml
- psutil
