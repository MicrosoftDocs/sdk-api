---
UID: NE:effects.PlayerState
title: PlayerState
author: windows-sdk-content
description: The PlayerState enumeration type provides some basic states of Windows Media Player.
old-location: wmp\playerstate.htm
old-project: WMP
ms.assetid: 7cd17639-e491-4066-838a-236554733874
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: PlayerState, PlayerState enumeration [Windows Media Player], effects/PlayerState, effects/pause_state, effects/play_state, effects/stop_state, enumeration [Windows Media Player], pause_state, play_state, stop_state, typedefenumPlayerState, wmp.playerstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - effects.h
api_name:
 - PlayerState
product: Windows
targetos: Windows
req.lib: Efswrt.h
req.dll: Efswrt.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# PlayerState enumeration


## -description



The <b>PlayerState</b> enumeration type provides some basic states of Windows Media Player.


<table>
<tr>
<th>
            Number
          </th>
<th>
            Description
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




### -field stop_state


### -field pause_state


### -field play_state


## -remarks



This enumeration is used by the <b>TimedLevel</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/a33d4cd1-e888-4ecd-9e6c-113febfefd99">TimedLevel</a>



<a href="https://msdn.microsoft.com/b54238a6-3d17-47b8-b650-bbe3473064da">Visualization Structures and Enumeration Types</a>
 

 

