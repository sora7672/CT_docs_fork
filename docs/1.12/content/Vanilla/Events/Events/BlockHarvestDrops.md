# BlockHarvestDropsEvent

The BlockHarvestDrops Event is fired whenever a block is about to drop its items.  
You can modify the block list as well as the overall drop chance. Set latter to 1 if you do all chance handling beforehand.

## Event Class
You will need to cast the event in the function header as this class:  
`crafttweaker.event.BlockHarvestDropsEvent`  
You can, of course, also [import](/AdvancedFunctions/Import/) the class before and use that name then.

## Event interface extensions
BlockHarvestDrops Events implement the following interfaces and are able to call all of their methods/getters/setters as well:

- [IBlockEvent](/Vanilla/Events/Events/IBlockEvent/)


## ZenGetters/ZenSetters
The following information can be retrieved from the event:

| ZenGetter        | ZenSetter     | Type                                                               |
|------------------|---------------|--------------------------------------------------------------------|
| `player`         |               | [IPlayer](/Vanilla/Players/IPlayer/)                               |
| `isPlayer`       |               | bool                                                               |
| `silkTouch`      |               | bool                                                               |
| `fortuneLevel`   |               | int                                                                |
| `drops`          | `drops`       | List<[WeightedItemStack](/Vanilla/Items/WeightedItemStack/)\>      |
| `dropChance`     | `dropChance`  | float                                                              |

## ZenMethods
- `event.addItem(IItemStack)` Adds the Item to the droplist


## ZenGetters/ZenSetters/ZenMethodes from extensions
The following information can be retrieved from the event:
| ZenGetter       | ZenSetter       | Type                                              |
|-----------------|-----------------|---------------------------------------------------|
| `world`         |                 | [IWorld](/Vanilla/World/IWorld/)                  |
| `blockState`    |                 | [IBlockState](/Vanilla/Blocks/IBlockState/)       |
| `block`         |                 | [IBlock](/Vanilla/Blocks/IBlock/)                 |


## From extension of extension

| ZenGetter       | ZenSetter       | Type                                              |
|-----------------|-----------------|---------------------------------------------------|
| `position`      |                 | [IBlockPos](/Vanilla/World/IBlockPos/)            |
| `x`             |                 | int                                               |
| `y`             |                 | int                                               |
| `z`             |                 | int                                               |


## Adding an item to the list
You can either addAssign the list or use the method to add an item to the list:
```zenscript
event.drops += <minecraft:coal>;
event.addItem(<minecraft:coal>);
```
