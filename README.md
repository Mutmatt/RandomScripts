# Steam Dedicated Server Automation Tool
> This project is intended to help setup a Steam Dedicated Server in an automated fashion.
There are some assumptions that we are making that will aid in making it easier to code but, generally, this script will do all the heavy lifting for you.

### Parameters available
* `-game "game"`
This is the game mode that we will be using. Right now we only support Garry's Mod so the gamemodes will be under that (sandbox, prop_hunt, terrortown, etc.) (Default: `prop_hunt`)
* `-serverName "Killing_town"`
This will be the name that will show up as your server name. If you include a space it will be converted to an `_`, spaces are *_not_* allowed but we protect that issue. (Default: `Tucker_Smells`)
* `-map "ph_example"`
This is the starting map for the game. You can change this after you start the game too. (Default... this will pick a random map based on the gamemode that is selected, so prop_hunt: `ph_*`, terrortown: `ttt_*`, etc.)
* `-installLocation "C:\install"`
This is the location on your computer that we will be installing the server. (Default: `C:\sourceServer`)
* `-forceUpdate 1`
This will force objhunt (currently only this) to update. This is important because we use the source code version of this game mode and not the workshop version so there may be broken things and we, most likely, want latest. (Default: `0`/`false`)

### Example run setup
`.\SetupAndRunGModDS.ps1 -game prop_hunt -serverName Eric_Smells -forceUpdate 1`

`.\SetupAndRunGModDS.ps1`
