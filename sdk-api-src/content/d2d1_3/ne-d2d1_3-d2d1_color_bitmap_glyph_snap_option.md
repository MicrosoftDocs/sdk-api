---
UID: NE:d2d1_3.D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION
title: D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION (d2d1_3.h)
description: Specifies the pixel snapping policy when rendering color bitmap glyphs.
helpviewer_keywords: ["D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION","D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION enumeration [Direct2D]","D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DEFAULT","D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DISABLE","d2d1_3/D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION","d2d1_3/D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DEFAULT","d2d1_3/D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DISABLE","direct2d.d2d1_color_bitmap_glyph_snap_option"]
old-location: direct2d\d2d1_color_bitmap_glyph_snap_option.htm
tech.root: Direct2D
ms.assetid: 14D99AFE-8072-4EAC-8932-6BD8D6EACB48
ms.date: 12/05/2018
ms.keywords: D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION, D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION enumeration [Direct2D], D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DEFAULT, D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DISABLE, d2d1_3/D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION, d2d1_3/D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DEFAULT, d2d1_3/D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DISABLE, direct2d.d2d1_color_bitmap_glyph_snap_option
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION
 - d2d1_3/D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1_3.h
api_name:
 - D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION
---

# D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION enumeration


## -description

Specifies the pixel snapping policy when rendering color bitmap glyphs.

## -enum-fields

### -field D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DEFAULT:0

Color bitmap glyph positions are snapped to the nearest pixel if the bitmap
          resolution matches that of the device context.

### -field D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_DISABLE:1

Color bitmap glyph positions are not snapped.

### -field D2D1_COLOR_BITMAP_GLYPH_SNAP_OPTION_FORCE_DWORD:0xffffffff

