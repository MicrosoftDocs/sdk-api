---
UID: NE:gdiplusenums.DriverStringOptions
title: DriverStringOptions (gdiplusenums.h)
description: The DriverStringOptions enumeration specifies the spacing, orientation, and quality of the rendering for driver strings.
helpviewer_keywords: ["DriverStringOptions","DriverStringOptions enumeration [GDI+]","DriverStringOptionsCmapLookup","DriverStringOptionsLimitSubpixel","DriverStringOptionsRealizedAdvance","DriverStringOptionsVertical","_gdiplus_ENUM_DriverStringOptions","gdiplus._gdiplus_ENUM_DriverStringOptions","gdiplusenums/DriverStringOptions","gdiplusenums/DriverStringOptionsCmapLookup","gdiplusenums/DriverStringOptionsLimitSubpixel","gdiplusenums/DriverStringOptionsRealizedAdvance","gdiplusenums/DriverStringOptionsVertical"]
old-location: gdiplus\_gdiplus_ENUM_DriverStringOptions.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\driverstringoptions.htm
ms.date: 12/05/2018
ms.keywords: DriverStringOptions, DriverStringOptions enumeration [GDI+], DriverStringOptionsCmapLookup, DriverStringOptionsLimitSubpixel, DriverStringOptionsRealizedAdvance, DriverStringOptionsVertical, _gdiplus_ENUM_DriverStringOptions, gdiplus._gdiplus_ENUM_DriverStringOptions, gdiplusenums/DriverStringOptions, gdiplusenums/DriverStringOptionsCmapLookup, gdiplusenums/DriverStringOptionsLimitSubpixel, gdiplusenums/DriverStringOptionsRealizedAdvance, gdiplusenums/DriverStringOptionsVertical
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
 - DriverStringOptions
 - gdiplusenums/DriverStringOptions
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
 - DriverStringOptions
---

# DriverStringOptions enumeration


## -description

The <b>DriverStringOptions</b> enumeration specifies the spacing, orientation, and quality of the rendering for driver strings.

## -enum-fields

### -field DriverStringOptionsCmapLookup:1

Specifies that the string array contains Unicode character values. 
			If this flag is not set, each value in array is interpreted as an index to a font glyph that defines a character to be displayed.

### -field DriverStringOptionsVertical:2

Specifies that the string is displayed vertically.

### -field DriverStringOptionsRealizedAdvance:4

Specifies that the glyph positions are calculated from the position of the first glyph. If this flag is not set, the glyph positions are obtained from an array of coordinates.

### -field DriverStringOptionsLimitSubpixel:8

Specifies that less memory should be used for cache of antialiased glyphs. This also produces lower quality. If this flag isn't set, more memory is used, but the quality is higher.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-antialiasing-with-text-use">Antialiasing with Text</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawdriverstring">Graphics::DrawDriverString</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-measuredriverstring">Graphics::MeasureDriverString</a>
