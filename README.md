# My Shared Compendia

A Foundry VTT module to share Data between worlds via compendia as explained by u/solfolango on
r/FoundryVTT; [here](https://www.reddit.com/r/FoundryVTT/comments/fvw3c7/how_to_create_a_tiny_module_for_shared_content/ "here").
It's not hard to do, but you can jumpstart your efforts by using this module.

## Installation

1. Go to the Add-on Modules tab within the FoundryVTT Configuration and Setup page.
2. Click the `Install Module` button.
3. Paste the Module's [Manifest URL](https://github.com/npiani/My-Shared-Compendia/releases/download/1.0.0/module.json)
   into the `Manifest URL` field.
4. Click the `Install` button.

| WARNING: If you update this module, FoundryVTT will erase your compendia. |
|---------------------------------------------------------------------------|

### Preventing Module Update

* Option 1 (easier): Locking your module:
    1. Go to the Add-on Modules tab within the FoundryVTT Configuration and Setup page.
    2. Find this module (My Shared Compendia) in the list, and click the padlock icon.
        * Unlocked:  
          ![unlocked-module](resources/images/unlocked-module.webp)
        * Locked:  
          ![locked-module](resources/images/locked-module.webp)
* Option 2: Updating your `module.json` file:
    1. Go to the Module's installation folder within foundry (`~/Data/modules/My Shared Compendia`) and update the `module.json` file.
    2. Remove lines 68-69 (`download` and `manifest`) and save the file.
    3. Restart Foundry to reload the module.

### Unlock your Compendia!

*Remember* that you need to unlock your compendia to be able to add things to them.

## Default Setup

This module comes with 8 Default compendia:

- `Actors (shared)` ([Actor](https://foundryvtt.com/api/Actor.html "Actor"))
- `Monsters (shared)` ([Actor](https://foundryvtt.com/api/Actor.html "Actor"))
- `Items (shared)` ([Item](https://foundryvtt.com/api/Item.html "Item"))
- `Scenes (shared)` ([Scene](https://foundryvtt.com/api/Scene.html "Scene"))
- `Journal Entries (shared)` ([JournalEntry](https://foundryvtt.com/api/JournalEntry.html "JournalEntry"))
- `Macros (shared)` ([Macro](https://foundryvtt.com/api/Macro.html "Macro"))
- `Roll Tables (shared)` ([RollTable](https://foundryvtt.com/api/RollTable.html "RollTable"))
- `Playlists (shared)` ([Playlist](https://foundryvtt.com/api/Playlist.html "Playlist"))

## Customize

To change the default setup, edit the `module.json` file. All compendia are defined within the "packs" attribute beginning with line 10.

There's a sample for each compendium Type - so start there. Delete or change as you see fit and/or [fork](https://github.com/npiani/My-Shared-Compendia/fork) for your convenience.

### Classes, Feats or Features

There are no compendium Types for Classes, Feats, Features in Foundry, so the `Item` type is generally used for these. For Example:

```json
{
  "packs": [
    {
      "name": "feats",
      "label": " Feats (shared)",
      "path": "packs/feats.db",
      "module": "my-shared-compendia",
      "type": "Item"
    },
    {
      "name": "classes",
      "label": "Classes (shared)",
      "path": "packs/classes.db",
      "module": "my-shared-compendia",
      "type": "Item"
    },
    {
      "name": "class-features",
      "label": "Class Features (shared)",
      "path": "packs/class-features.db",
      "module": "my-shared-compendia",
      "type": "Item"
    }
  ]
}
```

## Dependencies

There a no known dependencies, but using [Compendium Folders](https://github.com/earlSt1/vtt-compendium-folders "Compendium Folders") is highly recommended.

# Credits
Credit goes to [stschoelzel](https://github.com/stschoelzel) for the [initial module](https://github.com/stschoelzel/My-Shared-Compendia). I forked it, cleaned it up, and made it more suited to my own needs.

<img alt="GitHub all releases" src="https://img.shields.io/github/downloads/npiani/My-Shared-Compendia/total">
