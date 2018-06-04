---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0001 enumeration


## -description


Describes the tiling behavior of a tile brush.


## -enum-fields




### -field XPS_TILE_MODE_NONE

Only the base tile is drawn.


### -field XPS_TILE_MODE_TILE

First, the base tile is drawn. Next, the remaining area is filled by repeating the base tile such that the right edge of one tile is adjacent to the left edge of the next, and similarly for bottom and top.


### -field XPS_TILE_MODE_FLIPX

The same as <b>XPS_TILE_MODE_TILE</b>, but alternate columns of tiles are flipped horizontally.


### -field XPS_TILE_MODE_FLIPY

The same as <b>XPS_TILE_MODE_TILE</b>, but alternate rows of tiles are flipped vertically.



### -field XPS_TILE_MODE_FLIPXY

The combination of the effects produced by <b>XPS_TILE_MODE_FLIPX</b> and <b>XPS_TILE_MODE_FLIPY</b>.



## -remarks



The following illustration shows the effect of each tile mode on how a tiled brush fills the output area.

<img alt="An illustration that shows different examples of different tile mode behaviors" src="../images/TileMode.png"/>



## -see-also




<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

