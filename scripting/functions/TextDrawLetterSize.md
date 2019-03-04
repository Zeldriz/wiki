---
title: TextDrawLetterSize
description: Sets the width and height of the letters.
tags: ["textdraw"]
---

# TextDrawLetterSize

## Description

Sets the width and height of the letters.

| Name    | Description            |
| ------- | ---------------------- |
| text    | The TextDraw to change |
| Float:x | Width of a char.       |
| Float:y | Height of a char.      |

## Returns

This function does not return any specific values.

## Examples

```c
new Text:MyTextdraw;
 
public OnGameModeInit()
{
    MyTextDraw = TextDrawCreate(100.0, 33.0,"Example TextDraw");
    TextDrawLetterSize(MyTextDraw, 3.2 ,5.1);
    return 1;
}
```

## Notes

::: tip

When using this function purely for the benefit of affecting the TextDraw box, multiply 'Y' by 0.135 to convert to TextDrawTextSize-like measurements. Hint: it is easier and extremely precise to use LD_SPAC:white sprite for box-only textdraws, TextDrawTextSize will have regular offsets.

:::

::: tip

If you want to change the letter size of a textdraw that is already shown, you don't have to recreate it. Simply use TextDrawShowForPlayer/TextDrawShowForAll after modifying the textdraw and the change will be visible.
Fonts appear to look the best with an X to Y ratio of 1 to 4 (e.g. if x is 0.5 then y should be 2).

:::

## Related Functions

- TextDrawCreate: Create a textdraw.
- TextDrawDestroy: Destroy a textdraw.
- TextDrawColor: Set the color of the text in a textdraw.
- TextDrawBoxColor: Set the color of the box in a textdraw.
- TextDrawBackgroundColor: Set the background color of a textdraw.
- TextDrawAlignment: Set the alignment of a textdraw.
- TextDrawFont: Set the font of a textdraw.
- TextDrawTextSize: Set the size of a textdraw box.
- TextDrawSetOutline: Choose whether the text has an outline.
- TextDrawSetShadow: Toggle shadows on a textdraw.
- TextDrawSetProportional: Scale the text spacing in a textdraw to a proportional ratio.
- TextDrawUseBox: Toggle if the textdraw has a box or not.
- TextDrawSetString: Set the text in an existing textdraw.
- TextDrawShowForPlayer: Show a textdraw for a certain player.
- TextDrawHideForPlayer: Hide a textdraw for a certain player.
- TextDrawShowForAll: Show a textdraw for all players.
- TextDrawHideForAll: Hide a textdraw for all players.