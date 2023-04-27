---
UID: NE:effects.PlayerState
title: PlayerState (effects.h)
description: The PlayerState enumeration type provides some basic states of Windows Media Player.
helpviewer_keywords: ["PlayerState","PlayerState enumeration [Windows Media Player]","effects/PlayerState","effects/pause_state","effects/play_state","effects/stop_state","enumeration [Windows Media Player]","pause_state","play_state","stop_state","typedefenumPlayerState","wmp.playerstate"]
old-location: wmp\playerstate.htm
tech.root: WMP
ms.assetid: 7cd17639-e491-4066-838a-236554733874
ms.date: 12/05/2018
ms.keywords: PlayerState, PlayerState enumeration [Windows Media Player], effects/PlayerState, effects/pause_state, effects/play_state, effects/stop_state, enumeration [Windows Media Player], pause_state, play_state, stop_state, typedefenumPlayerState, wmp.playerstate
req.header: effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player version 7.0 or later.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PlayerState
 - effects/PlayerState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - effects.h
api_name:
 - PlayerState
---

# PlayerState enumeration


## -description

The <b>PlayerState</b> enumeration type provides some basic states of Windows Media Player.


<table>
<tr>
<th>Number
          </th>
<th>Description
          </th>
</tr>
<tr>
<td>0</td>
<td>Stop state</td>
</tr>
<tr>
<td>1</td>
<td>Pause state</td>
</tr>
<tr>
<td>2</td>
<td>Play state</td>
</tr>
</table>

## -enum-fields

### -field stop_state:0

### -field pause_state:1

### -field play_state:2

## -remarks

This enumeration is used by the <b>TimedLevel</b> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/effects/ns-effects-timedlevel">TimedLevel</a>



<a href="/windows/desktop/WMP/visualization-structures-and-enumeration-types">Visualization Structures and Enumeration Types</a>
