# pr-slack-bot

A repo with the workflow for posting to slack when a pr is merged

To use: 
* Generate a Slack OAuth Token (see: <https://docs.celigo.com/hc/en-us/articles/7140655476507-How-to-create-an-app-and-retrieve-OAuth-token-in-Slack>
  - This involves creating a slack app
* Define an organization level secret: SLACK_BOT_USER_OAUTH_ACCESS_TOKEN with that value
* Define an organization level variable called TEAM_TO_CHANNEL which is a JSON object mapping the last nine characters of the repo (typically team name) to team channel
* Install the slack app in every team channel

Installing looks like this when successful:

<img width="468" alt="image" src="https://github.com/ucsb-cs156-s24/pr-slack-bot/assets/1119017/d7c92956-a53a-4bf4-bcf9-e3c981c43bba">


Example value for `TEAM_TO_CHANNEL`

```json
{
    "s24-4pm-1": "C06R8PWJ563",
    "s24-4pm-2": "C06RPB52YHG",
    "s24-4pm-3": "C06S2146S49",
    "s24-4pm-4": "C06S2156TL1",
    "s24-4pm-5": "C06SC4XSQL8",
    "s24-4pm-6": "C06R8Q1ST8F",
    "s24-4pm-7": "C06RPBBPPLJ",
    "s24-4pm-8": "C06SC52SKKJ",
    "s24-5pm-1": "C06RLDRFMRB",
    "s24-5pm-2": "C06SC553MLY",
    "s24-5pm-3": "C06S21ENK5X",
    "s24-5pm-4": "C06RP82BN9H",
    "s24-5pm-5": "C06RP83BA83",
    "s24-5pm-6": "C06RGNALUES",
    "s24-5pm-7": "C06RPBN3D8A",
    "s24-5pm-8": "C06RLE09SLV",
    "slack-bot":"C073MP35QFL"
}
```
 
