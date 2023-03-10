---
UID: NE:gdiplusenums.WrapMode
title: WrapMode (gdiplusenums.h)
description: The WrapMode enumeration specifies how repeated copies of an image are used to tile an area.
helpviewer_keywords: ["WrapMode","WrapMode enumeration [GDI+]","WrapModeClamp","WrapModeTile","WrapModeTileFlipX","WrapModeTileFlipXY","WrapModeTileFlipY","_gdiplus_ENUM_WrapMode","gdiplus._gdiplus_ENUM_WrapMode","gdiplusenums/WrapMode","gdiplusenums/WrapModeClamp","gdiplusenums/WrapModeTile","gdiplusenums/WrapModeTileFlipX","gdiplusenums/WrapModeTileFlipXY","gdiplusenums/WrapModeTileFlipY"]
old-location: gdiplus\_gdiplus_ENUM_WrapMode.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\wrapmode.htm
ms.date: 12/05/2018
ms.keywords: WrapMode, WrapMode enumeration [GDI+], WrapModeClamp, WrapModeTile, WrapModeTileFlipX, WrapModeTileFlipXY, WrapModeTileFlipY, _gdiplus_ENUM_WrapMode, gdiplus._gdiplus_ENUM_WrapMode, gdiplusenums/WrapMode, gdiplusenums/WrapModeClamp, gdiplusenums/WrapModeTile, gdiplusenums/WrapModeTileFlipX, gdiplusenums/WrapModeTileFlipXY, gdiplusenums/WrapModeTileFlipY
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - WrapMode
 - gdiplusenums/WrapMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - WrapMode
---

# WrapMode enumeration


## -description

The <b>WrapMode</b> enumeration specifies how repeated copies of an image are used to tile an area.

## -enum-fields

### -field WrapModeTile

Specifies tiling without flipping.

### -field WrapModeTileFlipX

Specifies that tiles are flipped horizontally as you move from one tile to the next in a row.

### -field WrapModeTileFlipY

Specifies that tiles are flipped vertically as you move from one tile to the next in a column.

### -field WrapModeTileFlipXY

Specifies that tiles are flipped horizontally as you move along a row and flipped vertically as you move along a column.

### -field WrapModeClamp

Specifies that no tiling takes place.

