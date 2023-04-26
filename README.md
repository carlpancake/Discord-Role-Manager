# Discord Role Manager Bot

Role Manager is a discord BOT that utilizes Google Sheets for the organization of a server's hierarchy and permissions.


## Details

This BOT allows for you to export and organize your roles in a Google Sheet in a very user friendly way.

Three requests are made per usage of !export. One for clearing the spreadsheet, one for updating the roles/permission titles and one for the permission values themselves, making it extremely light and difficult for it to hit the Google Docs quota limit.
## Installation - Add the BOT to your server

Paste this on your browser to invite the BOT to a server you manage. The BOT requires the Administrator permission.

```bash
https://discord.com/api/oauth2/authorize?client_id=823014411945377824&permissions=8&scope=bot
```
> Note: As of writing, link above does not work unless it is verified.

## Usage - BOT Commands

```python
!setuphelp # Instructions on how to set up the BOT for your server.

!configure # Add your server to the BOT's database, along with your Google Sheet.

!export # Export your server's roles and their permissions to your Google Sheet.
```

## Requirements (for Developers)

```python
# Regular Module Imports
from os import path, sys
# Discord API Imports
import discord
from discord.ext import commands
# Google Docs/Sheets API Imports
import gspread
from google.oauth2.service_account import Credentials
from googleapiclient.discovery import build
```

> Note: `google.oauth2.service_account` was changed from `oauth2client.service_account` to accomodate to the new Google's API OAuth 2.0

If your server requires you to add **Additional Python Packages** in the **STARTUP** tab, simply add these and the server will install them for you.

```
discord gspread google-auth google-api-python-client
```

![image](https://user-images.githubusercontent.com/115357798/234480208-95165aa0-bf44-4199-b363-bfb4f4e83ef1.png)

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)
