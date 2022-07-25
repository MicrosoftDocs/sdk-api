---
UID: NE:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0001
title: XPS_TILE_MODE (xpsobjectmodel.h)
description: Describes the tiling behavior of a tile brush.
helpviewer_keywords: ["XPS_TILE_MODE","XPS_TILE_MODE enumeration [XPS Documents and Packaging]","XPS_TILE_MODE_FLIPX","XPS_TILE_MODE_FLIPXY","XPS_TILE_MODE_FLIPY","XPS_TILE_MODE_NONE","XPS_TILE_MODE_TILE","xps.xps_tile_mode","xpsobjectmodel/XPS_TILE_MODE","xpsobjectmodel/XPS_TILE_MODE_FLIPX","xpsobjectmodel/XPS_TILE_MODE_FLIPXY","xpsobjectmodel/XPS_TILE_MODE_FLIPY","xpsobjectmodel/XPS_TILE_MODE_NONE","xpsobjectmodel/XPS_TILE_MODE_TILE"]
old-location: xps\xps_tile_mode.htm
tech.root: xps
ms.assetid: 59434771-6402-4b0f-b8b6-58a4dda0f836
ms.date: 12/05/2018
ms.keywords: XPS_TILE_MODE, XPS_TILE_MODE enumeration [XPS Documents and Packaging], XPS_TILE_MODE_FLIPX, XPS_TILE_MODE_FLIPXY, XPS_TILE_MODE_FLIPY, XPS_TILE_MODE_NONE, XPS_TILE_MODE_TILE, xps.xps_tile_mode, xpsobjectmodel/XPS_TILE_MODE, xpsobjectmodel/XPS_TILE_MODE_FLIPX, xpsobjectmodel/XPS_TILE_MODE_FLIPXY, xpsobjectmodel/XPS_TILE_MODE_FLIPY, xpsobjectmodel/XPS_TILE_MODE_NONE, xpsobjectmodel/XPS_TILE_MODE_TILE
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XPS_TILE_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0001
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0001
 - XPS_TILE_MODE
 - xpsobjectmodel/XPS_TILE_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel.h
api_name:
 - XPS_TILE_MODE
---

# XPS_TILE_MODE enumeration


## -description

Describes the tiling behavior of a tile brush.

## -enum-fields

### -field XPS_TILE_MODE_NONE:1

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

<img alt="An illustration that shows different examples of different tile mode behaviors" src="./images/TileMode.png"/>

## -see-also

<a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>

