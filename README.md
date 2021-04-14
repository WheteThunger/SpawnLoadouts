## Features

**This branch of the plugin only allows saving belt items. Further development will continue on the master branch.**

- Allows players to make their own spawn loadouts
- Allows settings a default loadout for new players

## Commands

- `loadout save` -- Saves the player's current inventory as their spawn loadout.
- `loadout setdefault` -- Saves the player's current inventory as the global default spawn loadout (applies to players who haven't saved a custom spawn loadout).
- `loadout reset` -- Resets the player's saved loadout to the global default loadout.

## Permissions

- `spawnloadouts.save` -- Required to use `/loadout save`
- `spawnloadouts.setdefault` -- Required to use `/loadout setdefault`
- `spawnloadouts.getloadout` -- Required to use redeem a loadout on spawn

## Configuration

Default configuration:

```json
{
  "DefaultLoadout": {
    "MainItems": [
      {
        "ItemShortName": "ammo.rifle",
        "Amount": 74,
        "ChildItems": [
          "weapon.mod.holosight"
        ]
      }
    ],
    "BeltItems": [
      {
        "ItemShortName": "rifle.ak"
      }
    ],
    "WornItems": [
      {
        "ItemShortName": "roadsign.gloves"
      },
      {
        "ItemShortName": "roadsign.kilt"
      },
      {
        "ItemShortName": "metal.facemask"
      }
    ]
  },
  "DisallowedItems": []
}
```

- `DefaultLoadout` -- Definition for the default loadout. This loadout can be changed with the command `loadout setdefault` for players with permission.
- `DisallowedItems` -- List of item short names that players are not allowed to save in their loadouts.
  - Example: `["explosive.timed", "ammo.rocket.basic"]`.

## Localization

```json
{
  "Error.NoPermission": "You don't have the permsission to do that.",
  "Error.Syntax": "Error: Invalid syntax.",
  "Command.SetDefault.Success": "Default loadout has <color=#bfff00>succesfully been set!</color>",
  "Command.Save.Success": "Loadout was <color=#bfff00>sucessfully saved!</color>",
  "Command.Reset.Success": "Loadout was <color=#bfff00>sucessfully reset!</color>"
}
```
