# Permission and Flag Nodes

## Permissions

| Permission Name | Command | Description |
| :-------------- | :-----: | :---------- |
| behr.essentials.back                 | /back        | Allows the player to teleport back to their previous location |
| behr.essentials.commandspy           | /commandspy  | Allows the player to enable or disable listening to player commands ran |
| behr.essentials.command.commandgrant | /commandspy  | Allows the player to grant permissions prompted through commandspy |
| behr.essentials.dynmap               | /dynmap      | Allows the player to get the link for the dynmap |
| behr.essentials.fly                  | /fly         | Allows the player to enable or disable flight |
| behr.essentials.flyspeed             | /flyspeed    | Allows the player to adjust their flight speed |
| behrry.essentials.gma                | /gma         | Allows the player to switch to adventure mode |
| behrry.essentials.gmc                | /gmc         | Allows the player to switch to creative mode |
| behrry.essentials.gms                | /gms         | Allows the player to switch to survival mode |
| behrry.essentials.gmsp               | /gmsp        | Allows the player to switch to spectator mode |
| behr.essentials.groundclean          | /groundclean | Allows the player to clear dropped items on the ground |
| behr.essentials.heal                 | /heal        | Allows the player to heal themselves or another player |
| behr.essentials.inventorysee         | /invsee      | Allows the player to view and edit in another player's inventory |
| behr.essentials.ip                   | /ip          | Allows the player to view another player's IP address |
| behr.essentials.lore                 | /lore        | Allows the player to adjust the lore on their held item |
| behr.essentials.message              | /msg         | Allows the player to message another player |
| behr.essentials.suicide              | /suicide     | Allows the player to commit suicide |
| behr.essentials.restart              | /restart     | Allows the player to restart the server |
| behr.essentials.teleport             | /teleport    | Allows the player to teleport to another player, or teleport a player to another player |
| behr.essentials.top                  | /top         | Allows the player to teleport to the highest block on at their location |
| behr.essentials.tpaccept             | /tpaccept    | Allows the player to accept a teleport request |
| behr.essentials.tpdecline            | /tpdecline   | Allows the player to decline a teleport request |
| behr.essentials.debugging            | /debug       | Allows the player to enable or disable debugging mode for debugging content |
| behr.essentials.location             | /location    | Allows the player to teleport to the notable locations saved |
| behr.essentials.reload               | /reload      | Allows the player to reload the scripts on the server |

## Flags & Yaml

### Yaml Files

Yaml files can be found [`[here]`](https://github.com/bGielinor/Gielinor-Development/tree/master/data/repo-link).

| Yaml Name | Directory | Description |
| :-------- | :-------: | :---------- |
| equipment       | data/repo-link/equipment.yml       | Container for all worn equipments and their properties |
| items           | data/repo-link/items.yml           | Container for all non-worn items and their properties |
| tree_repository | data/repo-link/tree_repository.yml | Container for tree schematic directories |
| castle_wars     | data/minigames/castle_wars.yml     | Container for Castle Wars notable objects and data |

### Global Flags

| Flag Name | Target | Object Type | Description |
| :-------- | :----: | :---------: | :---------- |
| gielinor.skills.<[skill]>.level                         | Player | ElementTag(Int) | Returns the level in the given `<[Skill]>` skill |
| gielinor.skills.<[skill]>.experience                    | Player | ElementTag(Int) | Returns the experience in the given `<[Skill]>` skill |
| gielinor.skills.<[skill]>.experience_requirement        | Player | ElementTag(Int) | Returns the experience required in the given `<[Skill]>` skill to the next level |
| behr.essentials.behredit.selection                      | Player | CuboidTag       | Returns the selection the player has selected |
| behr.essentials.behredit.selection_mode                 | Player | ElementTag      | Returns the selection mode for the player's BehrEdit Wand
| behr.essentials.behredit.pos1                           | Player | LocationTag     | Returns the left position selection |
| behr.essentials.behredit.pos2                           | Player | LocationTag     | Returns the right position selection |
| behr.essentials.behredit.posc                           | Player | LocationTag     | Returns the center (f) position selection |
| behr.essentials.behredit.monitor                        | Player | Boolean         | Returns `true` if the player is currently monitoring their BehrEdit Clipboard outline. |
| behr.message_rate_limit.behredit.clear_selection        | Player | Boolean         | Returns `true` if the player has received an initial prompt for clearing the BehrEdit Clipboard. |
| behr.message_rate_limit.behredit.clear_selection_repeat | Player | Boolean         | Returns `true` if the player has been told nothing interesting happens clearing an empty clipboard |
| behr.message_rate_limit.behredit.tree_hard_reset        | Player | Boolean         | Returns `true` if the player has been warned prior to a hard reset of the tree repository |
| behr.essentials.behredit.plant_mode                     | Player | Boolean         | Returns `true` if the player has enabled tree planting mode and is actively placing trees |
| behr.essentials.behredit.tree_plant_selection           | Player | ElementTag      | Returns the tree group that the player is actively placing in tree plant mode |
| behr.essentials.behredit.tree_plan_index                | Player | ElementTag(Int) | Returns the tree group index that the player is actively placing in tree plant mode |

### Commands

| Flag Name | Target | Command | Object Type | Description |
| :-------- | :----: | :-----: | :---------: | :---------- |
| behr.essentials.teleport.back               | Player | /back        | MapTag     | Returns a map of the locations by the world name and the locationtag to teleport back to after teleporting |
| behr.essentials.teleport.locations          | Player | (*Teleports) | MapTag     | Returns a map of locations by name and location for notable areas to teleport to |
| behr.essentials.worldprompt.load            | Player | /world       | Boolean    | Returns `true` if the player has received an initial prompt for loading a world |
| behr.essentials.worldprompt.unload          | Player | /world       | Boolean    | Returns `true` if the player has received an initial prompt for unloading a world |
| behr.essentials.worldprompt.create          | Player | /world       | Boolean    | Returns `true` if the player has received an initial prompt for creating a world |
| behr.essentials.worldprompt.destroy0        | Player | /world       | Boolean    | Returns `true` if the player has received an initial prompt for destroying a world |
| behr.essentials.worldprompt.destroy1        | Player | /world       | Boolean    | Returns `true` if the player has received an initial prompt for destroying a world, again, because please verify |
| behr.essentials.commandlistening            | Player | /commandspy  | Boolean    | Returns `true` if a player is listening to commands being ran |
| behr.essentials.command.permission_provided | Player | /commandspy  | ElementTag | Returns the formatted message fed into the command grant message |
| behr.essentials.tabofflinemode              | Player | /taboffline  | Boolean    | Returns `true` if the player has prompted to tab-complete offline players for PlayerName arguments |
| Behr.Essentials.Teleport.Requests           | Player | (*Teleports) | MapTag     | Returns a map of the players with a map of the teleport request by type and location | 
| behr.essentials.debugging                   | Player | /debug       | Boolean   | Returns `true` if the player has prompted to listen to debugging messages |
| behr.essentials.teleport.locations          | Server | /location    | MapTag     | Returns a map of notable locations by name and location |

* Commands referenced as `*Teleports` refer to multiple teleport commands universally

### Minigames

#### Castle War

| Flag Name | Target | Object Type | Description |
| :-------- | :----: | :---------: | :---------- |
| gielinor.message_rate_limit.castle_wars_equipment_requirement       | Player | Boolean            | Ratelimit for message sent when attempting to enter the game wearing hats, cloaks or helms |
| gielinor.message_rate_limit.castle_wars_wrong_respawn_door          | Player | Boolean            | Ratelimit for message sent when attempting to enter the wrong team respawn room |
| gielinor.message_rate_limit.castle_wars_respawn_door_with_flag      | Player | Boolean            | Ratelimit for message sent when attempting to enter the respawn room carrying the flag |
| gielinor.message_rate_limit.castle_wars_respawn_door                | Player | Boolean            | Ratelimit for message sent when attempting to use the respawn room doors too quickly |
| gielinor.message_rate_limit.castle_wars_respawn_door                | Player | Boolean            | Ratelimit for message sent when attempting to use the respawn room doors too quickly |
| gielinor.message_rate_limit.castle_wars_barricade_in_respawn        | Player | Boolean            | Ratelimit for message sent when attempting to place a barricade in the respawn room |
| gielinor.message_rate_limit.castle_wars_maximum_barricades_set      | Player | Boolean            | Ratelimit for message sent when attempting to place more barricades than the team's allowed barricades |
| gielinor.minigames.castle_wars.in_queue                             | Server | Boolean            | Returns `true` if Castle Wars has an active queue in process |
| gielinor.minigames.castle_wars.in_queue                             | Player | Boolean            | Returns `true` if the player is in the castle wars queue |
| gielinor.minigames.castle_wars.death_screen                         | Player | Boolean            | Returns `true` if the player has died and is on the death screen |
| gielinor.minigames.castle_wars.bandage_cooldown                     | Player | Boolean            | Returns `true` if the player has a bandage usage cooldown active |
| gielinor.minigames.castle_wars.potion_cooldown                      | Player | Boolean            | Returns `true` if the player has an explosive potion usage cooldown active |
| gielinor.minigames.castle_wars.barricade_cooldown                   | Player | Boolean            | Returns `true` if the player has a barricade usage cooldown active |
| gielinor.minigames.castle_wars.respawn_door_cooldown                | Player | Boolean            | Ratelimit for attempting to use the respawn room doors too quickly
| gielinor.minigames.castle_wars.team.red                             | Player | ElementTag         | Returns `true` if the player is on the `red` team `(*this is old usage and should be converted to a single flag*)` |
| gielinor.minigames.castle_wars.team.blue                            | Player | ElementTag         | Returns `true` if the player is on the `blue` team `(*this is old usage and should be converted to a single flag*)` |
| gielinor.minigames.castle_wars.flag_carrier                         | Player | Boolean            | Returns `true` if the player is carrying the opposing team's flag |
| gielinor.minigames.castle_wars.in_game                              | Server | Boolean            | Returns `true` if the player is in an active Castle Wars game |
| gielinor.minigames.castle_wars.flag_captured.red                    | Server | Boolean            | Returns `true` if the `red` team's flag has been captured |
| gielinor.minigames.castle_wars.flag_captured.blue                   | Server | Boolean            | Returns `true` if the `blue` team's flag has been captured |
| gielinor.minigames.castle_wars.start_time                           | Server | DurationTag        | Returns the duration that the queue has until the next game starts |
| gielinor.minigames.castle_wars.players                              | Server | ListTag(PlayerTag) | Returns the list of players in the game |
| gielinor.minigames.castle_wars.in_game                              | Server | Boolean            | Returns `true` if the Castle Wars game is active |
| gielinor.minigames.castle_wars.score.red                            | Server | ElementTag(Int)    | Returns the score for the red team |
| gielinor.minigames.castle_wars.score.blue                           | Server | ElementTag(Int)    | Returns the score for the blue team |
| gielinor.minigames.castle_wars.active_queue                         | Server | QueueTag           | Returns the active queue for the Castle Wars game |
| gielinor.minigames.castle_wars.timer                                | Server | DurationTag        | Returns the duration remaining for the active Castle Wars game |
| gielinor.minigames.castle_wars.waiting_box                          | Server | ElementTag         | Returns the queue waiting bossbar font box
| gielinor.minigames.castle_wars.barricade_damage_cooldown.<[entity]> | Server | Boolean            | Returns `true` if the barricade entity has a damage cooldown |
| gielinor.minigames.castle_wars.barricade_health_display.<[entity]>  | Server | Boolean            | Returns `true` if the barricade entity has a healthbar active |
| gielinor.minigames.castle_wars.rockfall.<[team]>.<[axis]>.fallen    | Server | Boolean            | Returns `true` if the rockfall at this location has fallen |
| gielinor.minigames.castle_wars.rockfall.<[team]>.<[axis]>.health    | Server | ElementTag         | Returns the health of the rockfall at this location |
| gielinor.play_effects.castle_wars.hub                               | Server | Boolean            | Returns `true` if players are within proximity to activate portal particle effects for the castle wars hub |
| gielinor.statistics.minigames.castle_wars.red.won_games             | Server | ElementTag         | Returns the amount of games the Red team has won in the Castle Wars minigame. |
| gielinor.statistics.minigames.season.<[season]>.<[team]>            | Server | ElementTag         | Returns the amount of games the `<[team]>` has won this `<[season]>`, where season is a `year_season` format, eg: `2020_summer` |
| gielinor.statistics.minigames.castle_wars.won_games                 | Player | ElementTag         | Returns the amount of games the player has won in the Castle Wars minigame. |
| gielinor.statistics.minigames.castle_wars.lost_games                | Player | ElementTag         | Returns the amount of games the player has lost in the Castle Wars minigame. |
| gielinor.statistics.minigames.castle_wars.games_played              | Player | ElementTag         | Returns the amount of games the player has played in the Castle Wars minigame. |
