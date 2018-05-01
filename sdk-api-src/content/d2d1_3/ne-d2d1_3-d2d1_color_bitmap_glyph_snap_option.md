---
UID: NE:d2d1_3.D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION
title: D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION
author: windows-driver-content
description: Specifies the pixel snapping policy when rendering color bitmap glyphs.
old-location: direct2d\d2d1_color_bitmap_glyph_snap_option.htm
old-project: Direct2D
ms.assetid: 14D99AFE-8072-4EAC-8932-6BD8D6EACB48
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION, D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION enumeration [Direct2D], D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DEFAULT, D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DISABLE, d2d1_3/D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION, d2d1_3/D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DEFAULT, d2d1_3/D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DISABLE, direct2d.d2d1_color_bitmap_glyph_snap_option
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d2d1_3.h
api_name:
-	D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION enumeration


## -description


Specifies the pixel snapping policy when rendering color bitmap glyphs.


## -enum-fields




### -field D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DEFAULT

Color bitmap glyph positions are snapped to the nearest pixel if the bitmap
          resolution matches that of the device context.


### -field D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DISABLE

Color bitmap glyph positions are not snapped.


### -field D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_FORCE_DWORD



