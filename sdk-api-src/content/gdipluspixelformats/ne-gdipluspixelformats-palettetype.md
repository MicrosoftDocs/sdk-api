---
UID: NE:gdipluspixelformats.PaletteType
title: PaletteType (gdipluspixelformats.h)
description: The PaletteType enumeration is used by the Bitmap::InitializePalette and Bitmap::ConvertFormat methods of the Bitmap class. The members of the enumeration identify several standard color palette formats.
helpviewer_keywords: ["PaletteType","PaletteType enumeration [GDI+]","PaletteTypeCustom","PaletteTypeFixedBW","PaletteTypeFixedHalftone125","PaletteTypeFixedHalftone216","PaletteTypeFixedHalftone252","PaletteTypeFixedHalftone256","PaletteTypeFixedHalftone27","PaletteTypeFixedHalftone64","PaletteTypeFixedHalftone8","PaletteTypeOptimal","_gdiplus_ENUM_PaletteType","gdiplus._gdiplus_ENUM_PaletteType","gdipluspixelformats/PaletteType","gdipluspixelformats/PaletteTypeCustom","gdipluspixelformats/PaletteTypeFixedBW","gdipluspixelformats/PaletteTypeFixedHalftone125","gdipluspixelformats/PaletteTypeFixedHalftone216","gdipluspixelformats/PaletteTypeFixedHalftone252","gdipluspixelformats/PaletteTypeFixedHalftone256","gdipluspixelformats/PaletteTypeFixedHalftone27","gdipluspixelformats/PaletteTypeFixedHalftone64","gdipluspixelformats/PaletteTypeFixedHalftone8","gdipluspixelformats/PaletteTypeOptimal"]
old-location: gdiplus\_gdiplus_ENUM_PaletteType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\palettetype.htm
ms.date: 12/05/2018
ms.keywords: PaletteType, PaletteType enumeration [GDI+], PaletteTypeCustom, PaletteTypeFixedBW, PaletteTypeFixedHalftone125, PaletteTypeFixedHalftone216, PaletteTypeFixedHalftone252, PaletteTypeFixedHalftone256, PaletteTypeFixedHalftone27, PaletteTypeFixedHalftone64, PaletteTypeFixedHalftone8, PaletteTypeOptimal, _gdiplus_ENUM_PaletteType, gdiplus._gdiplus_ENUM_PaletteType, gdipluspixelformats/PaletteType, gdipluspixelformats/PaletteTypeCustom, gdipluspixelformats/PaletteTypeFixedBW, gdipluspixelformats/PaletteTypeFixedHalftone125, gdipluspixelformats/PaletteTypeFixedHalftone216, gdipluspixelformats/PaletteTypeFixedHalftone252, gdipluspixelformats/PaletteTypeFixedHalftone256, gdipluspixelformats/PaletteTypeFixedHalftone27, gdipluspixelformats/PaletteTypeFixedHalftone64, gdipluspixelformats/PaletteTypeFixedHalftone8, gdipluspixelformats/PaletteTypeOptimal
req.header: gdipluspixelformats.h
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
 - PaletteType
 - gdipluspixelformats/PaletteType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - GdiplusPixelFormats.h
api_name:
 - PaletteType
---

# PaletteType enumeration


## -description

The  <b>PaletteType</b> enumeration is used by the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-initializepalette">Bitmap::InitializePalette</a> and <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-convertformat">Bitmap::ConvertFormat</a> methods of the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> class. The members of the enumeration identify several standard color palette formats.

## -enum-fields

### -field PaletteTypeCustom:0

An arbitrary custom palette provided by the caller.

### -field PaletteTypeOptimal:1

An palette of colors that are optimal for a particular bitmap. To create an optimal palette, pass PaletteTypeOptimal, the number of colors you want in the palette, and the address of a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object to the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-initializepalette">Bitmap::InitializePalette</a> method.

### -field PaletteTypeFixedBW:2

A palette that has two colors. This palette type is suitable for bitmaps that store 1 bit per pixel.

### -field PaletteTypeFixedHalftone8:3

A palette based on two intensities each (off or full) for the red, green, and blue channels. Also contains the 16 colors of the system palette. Because all eight of the on/off combinations of red, green, and blue are already in the system palette, this palette is the same as the system palette. This palette type is suitable for bitmaps that store 4 bits per pixel.

### -field PaletteTypeFixedHalftone27:4

A palette based on three intensities each for the red, green, and blue channels. Also contains the 16 colors of the system palette. Eight of the 16 system palette colors are among the 27 three-intensity combinations of red, green, and blue, so the total number of colors in the palette is 35. If the palette also includes the transparent color, the total number of colors is 36.

### -field PaletteTypeFixedHalftone64:5

A palette based on four intensities each for the red, green, and blue channels. Also contains the 16 colors of the system palette. Eight of the 16 system palette colors are among the 64 four-intensity combinations of red, green, and blue, so the total number of colors in the palette is 72. If the palette also includes the transparent color, the total number of colors is 73.

### -field PaletteTypeFixedHalftone125:6

A palette based on five intensities each for the red, green, and blue channels. Also contains the 16 colors of the system palette. Eight of the 16 system palette colors are among the 125 five-intensity combinations of red, green, and blue, so the total number of colors in the palette is 133. If the palette also includes the transparent color, the total number of colors is 134.

### -field PaletteTypeFixedHalftone216:7

A palette based on six intensities each for the red, green, and blue channels. Also contains the 16 colors of the system palette. Eight of the 16 system palette colors are among the 216 six-intensity combinations of red, green, and blue, so the total number of colors in the palette is 224. If the palette also includes the transparent color, the total number of colors is 225. This palette is sometimes called the Windows halftone palette or the Web palette.

### -field PaletteTypeFixedHalftone252:8

A palette based on 6 intensities of red, 7 intensities of green, and 6 intensities of blue. The system palette is not included. The total number of colors is 252. If the palette also includes the transparent color, the total number of colors is 253.

### -field PaletteTypeFixedHalftone256:9

A palette based on 8 intensities of red, 8 intensities of green, and 4 intensities of blue. The system palette is not included. The total number of colors is 256. If the transparent color is included in this palette, it must replace one of the RGB combinations.
