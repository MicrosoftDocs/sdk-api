---
UID: NE:gdiplusimaging.ItemDataPosition
title: ItemDataPosition (gdiplusimaging.h)
description: The ItemDataPosition enumeration is used to specify the location of custom metadata in an image file.
helpviewer_keywords: ["ItemDataPosition","ItemDataPosition enumeration [GDI+]","ItemDataPositionAfterBits","ItemDataPositionAfterHeader","ItemDataPositionAfterPalette","_gdiplus_ENUM_ItemDataPosition","gdiplus._gdiplus_ENUM_ItemDataPosition","gdiplusimaging/ItemDataPosition","gdiplusimaging/ItemDataPositionAfterBits","gdiplusimaging/ItemDataPositionAfterHeader","gdiplusimaging/ItemDataPositionAfterPalette"]
old-location: gdiplus\_gdiplus_ENUM_ItemDataPosition.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\itemdataposition.htm
ms.date: 12/05/2018
ms.keywords: ItemDataPosition, ItemDataPosition enumeration [GDI+], ItemDataPositionAfterBits, ItemDataPositionAfterHeader, ItemDataPositionAfterPalette, _gdiplus_ENUM_ItemDataPosition, gdiplus._gdiplus_ENUM_ItemDataPosition, gdiplusimaging/ItemDataPosition, gdiplusimaging/ItemDataPositionAfterBits, gdiplusimaging/ItemDataPositionAfterHeader, gdiplusimaging/ItemDataPositionAfterPalette
req.header: gdiplusimaging.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - ItemDataPosition
 - gdiplusimaging/ItemDataPosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - GdiplusImaging.h
api_name:
 - ItemDataPosition
---

# ItemDataPosition enumeration


## -description

The <b>ItemDataPosition</b> enumeration is used to specify the location of custom metadata in an image file.

## -enum-fields

### -field ItemDataPositionAfterHeader:0x0

Specifies that custom metadata is stored after the file header. Valid for JPEG, PNG, and GIF.

### -field ItemDataPositionAfterPalette:0x1

Specifies that custom metadata is stored after the palette. Valid for PNG.

### -field ItemDataPositionAfterBits:0x2

Specifies that custom metadata is stored after the pixel data. Valid for GIF and PNG.

## -remarks

GDI+ supports custom metadata for JPEG, PNG, and GIF image files.

## -see-also

<a href="/previous-versions/ms534468(v=vs.85)">ImageItemData</a>
