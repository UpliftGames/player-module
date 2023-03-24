# player-module
Packaged format of the Roblox PlayerModule for use with Wally

This repo pulls the PlayerModule and packages it in a format that is compatible with wally.

The repository is setup to pull the PlayerModule every 12 hours and update if out of date.

## Package interface

Info on the interface of this package can be found [here](https://github.com/UpliftGames/pull-player-scripts/blob/main/cli/PlayerScripts/PlayerModule/README.md).

tl;dr:

```Lua
-- returns either the patched or unpatched version the PlayerModule
Package.get(patched: boolean): ModuleScript

-- returns a copy of either the patched or unpatched version the PlayerModule
Package.getCopy(patched: boolean): ModuleScript

-- replaces the PlayerModule under StarterPlayer.StarterPlayerScripts 
-- with the provided module script
Package.replace(playerModule: ModuleScript)
```

## Where's the source?

The source is currently pulled to the release branch to keep the main branch free of any automated changes.

The only important file in this repo is [release.yml](.github/workflows/release.yml). The heavy lifting is done by this [tool](https://github.com/UpliftGames/pull-player-scripts).