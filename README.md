# Bingo Bot

LittleBigPlanet speedrunning race bot for Discord
(no bingo functionality)

## Setup

[Set up a Discord bot](https://discord.com/developers/applications). Enable Application > Bot > Server Members Intent.

Install Node.js (latest version to avoid issues)

Get build tools
* Windows: Install "VC++ 2015.3 v14.00 (v140) toolset for desktop" through VS Installer
* Linux: `sudo apt-get install build-essential`

Get dependencies

```
npm i
```

Create discord_auth.json in the bingo-bot folder with your auth token

```json
{
  "token": "discord auth token goes here"
}
```

Run bot.

```
npm start
```

## Commands

**Pre-race commands**
* `race`/`r` – Starts a new race, or joins the currently open race.
* `quit`/`q` – Leaves the race.
* `category [<game name> /] <category name>` – Sets the (game /) category.
* `ready`/`r` – Indicates that you're ready to start.
* `unready`/`ur` – Indicates that you're not actually ready.

**Mid-race commands**
* `done`/`d` – Indicates that you/your team finished.
* `undone`/`ud` – Indicates that you didn't actually finish.
* `forfeit`/`f` – Drops you/your team out of the race.
* `unforfeit`/`uf` – Rejoins the race after you forfeited.

**Co-op-race commands**
* `team [teamof] <@​entrant or user ID 1> […]` – Moves entrants/other teams into your team.
* `teamname [<team name>]` – Changes/resets your team's name.
* `unteam` – Leaves your current team.
* `unteamall` – Disbands all current teams.
* `randomteams [<team size>]` – Randomly assigns entrants to teams of the given size.

**IL-race commands**
* `ilresults` – Shows the ILs that have been raced so far in this series.
* `level <level name>` – Sets the level.

**Stat commands**
* `status`/`s` – Shows the current race status.
* `result [<race ID>]` – Shows the results of the specified race ID or the last race.
* `leaderboard <game name> / <category name>` – Shows the Elo leaderboard for the current/given game / category.
* `me <game name>` – Shows your race stats for a game.
* `runner <@​member or user ID> <game name>` – Shows a member's race stats.

**Other commands**
* `help [<command name>]` – Shows a list of commands or details on one command.
* `server <server name or ID> <command>` – In DMs, calls a command on the specified server.

**Moderator-only commands**
* `clearrace` – Ends the race without recording any results.
* `as <@​member or ID> <command>` – Calls a command as the specified user.
