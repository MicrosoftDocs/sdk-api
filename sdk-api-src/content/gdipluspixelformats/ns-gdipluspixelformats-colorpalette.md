---
UID: NS:gdipluspixelformats.ColorPalette
title: ColorPalette (gdipluspixelformats.h)
description: The ColorPalette structure defines an array of colors that make up a color palette. The colors are 32-bit ARGB colors.
helpviewer_keywords: ["ColorPalette","ColorPalette structure [GDI+]","_gdiplus_STRUC_ColorPalette","gdiplus._gdiplus_STRUC_ColorPalette","gdipluspixelformats/ColorPalette"]
old-location: gdiplus\_gdiplus_STRUC_ColorPalette.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colorpalette.htm
ms.date: 12/05/2018
ms.keywords: ColorPalette, ColorPalette structure [GDI+], _gdiplus_STRUC_ColorPalette, gdiplus._gdiplus_STRUC_ColorPalette, gdipluspixelformats/ColorPalette
req.header: gdipluspixelformats.h
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
 - ColorPalette
 - gdipluspixelformats/ColorPalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluspixelformats.h
api_name:
 - ColorPalette
---

# ColorPalette structure


## -description

The <b>ColorPalette</b> structure defines an array of colors that make up a color palette. The colors are 32-bit ARGB colors.

## -struct-fields

### -field Flags

Type: <b>UINT</b>

Combination of flags from the <a href="/windows/desktop/api/gdipluspixelformats/ne-gdipluspixelformats-paletteflags">PaletteFlags</a> enumeration.

### -field Count

Type: <b>UINT</b>

Number of elements in the <b>Entries</b> array.

### -field Entries

Type: <b>ARGB[1]</b>

Array of ARGB colors.

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpalette">Image::GetPalette</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-setpalette">Image::SetPalette</a>



<a href="/windows/desktop/gdiplus/-gdiplus-types-of-bitmaps-about">Types of Bitmaps</a>