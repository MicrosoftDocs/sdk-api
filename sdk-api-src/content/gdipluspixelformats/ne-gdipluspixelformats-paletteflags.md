---
UID: NE:gdipluspixelformats.PaletteFlags
title: PaletteFlags (gdipluspixelformats.h)
description: The PaletteFlags enumeration indicates attributes of the color data in a palette.
helpviewer_keywords: ["PaletteFlags","PaletteFlags enumeration [GDI+]","PaletteFlagsGrayScale","PaletteFlagsHalftone","PaletteFlagsHasAlpha","_gdiplus_ENUM_PaletteFlags","gdiplus._gdiplus_ENUM_PaletteFlags","gdipluspixelformats/PaletteFlags","gdipluspixelformats/PaletteFlagsGrayScale","gdipluspixelformats/PaletteFlagsHalftone","gdipluspixelformats/PaletteFlagsHasAlpha"]
old-location: gdiplus\_gdiplus_ENUM_PaletteFlags.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\paletteflags.htm
ms.date: 12/05/2018
ms.keywords: PaletteFlags, PaletteFlags enumeration [GDI+], PaletteFlagsGrayScale, PaletteFlagsHalftone, PaletteFlagsHasAlpha, _gdiplus_ENUM_PaletteFlags, gdiplus._gdiplus_ENUM_PaletteFlags, gdipluspixelformats/PaletteFlags, gdipluspixelformats/PaletteFlagsGrayScale, gdipluspixelformats/PaletteFlagsHalftone, gdipluspixelformats/PaletteFlagsHasAlpha
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
 - PaletteFlags
 - gdipluspixelformats/PaletteFlags
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
 - PaletteFlags
---

# PaletteFlags enumeration


## -description

The <b>PaletteFlags</b> enumeration indicates attributes of the color data in a palette.

## -enum-fields

### -field PaletteFlagsHasAlpha:0x0001

Indicates that one or more of the palette entries contains alpha (transparency) information.

### -field PaletteFlagsGrayScale:0x0002

Indicates that the palette contains only grayscale entries.

### -field PaletteFlagsHalftone:0x0004

Indicates that the palette is the Windows halftone palette.

