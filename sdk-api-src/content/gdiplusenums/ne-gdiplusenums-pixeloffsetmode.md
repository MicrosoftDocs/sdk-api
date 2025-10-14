---
UID: NE:gdiplusenums.PixelOffsetMode
title: PixelOffsetMode (gdiplusenums.h)
description: The PixelOffsetMode enumeration specifies the pixel offset mode of a Graphics object. This enumeration is used by the Graphics::GetPixelOffsetMode and Graphics::SetPixelOffsetMode methods of the Graphics class.
helpviewer_keywords: ["PixelOffsetMode","PixelOffsetMode enumeration [GDI+]","PixelOffsetModeDefault","PixelOffsetModeHalf","PixelOffsetModeHighQuality","PixelOffsetModeHighSpeed","PixelOffsetModeInvalid","PixelOffsetModeNone","_gdiplus_ENUM_PixelOffsetMode","gdiplus._gdiplus_ENUM_PixelOffsetMode","gdiplusenums/PixelOffsetMode","gdiplusenums/PixelOffsetModeDefault","gdiplusenums/PixelOffsetModeHalf","gdiplusenums/PixelOffsetModeHighQuality","gdiplusenums/PixelOffsetModeHighSpeed","gdiplusenums/PixelOffsetModeInvalid","gdiplusenums/PixelOffsetModeNone"]
old-location: gdiplus\_gdiplus_ENUM_PixelOffsetMode.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\pixeloffsetmode.htm
ms.date: 12/05/2018
ms.keywords: PixelOffsetMode, PixelOffsetMode enumeration [GDI+], PixelOffsetModeDefault, PixelOffsetModeHalf, PixelOffsetModeHighQuality, PixelOffsetModeHighSpeed, PixelOffsetModeInvalid, PixelOffsetModeNone, _gdiplus_ENUM_PixelOffsetMode, gdiplus._gdiplus_ENUM_PixelOffsetMode, gdiplusenums/PixelOffsetMode, gdiplusenums/PixelOffsetModeDefault, gdiplusenums/PixelOffsetModeHalf, gdiplusenums/PixelOffsetModeHighQuality, gdiplusenums/PixelOffsetModeHighSpeed, gdiplusenums/PixelOffsetModeInvalid, gdiplusenums/PixelOffsetModeNone
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
 - PixelOffsetMode
 - gdiplusenums/PixelOffsetMode
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
 - PixelOffsetMode
---

# PixelOffsetMode enumeration


## -description

The <b>PixelOffsetMode</b> enumeration specifies the pixel offset mode of a 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. This enumeration is used by the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getpixeloffsetmode">Graphics::GetPixelOffsetMode</a> and <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setpixeloffsetmode">Graphics::SetPixelOffsetMode</a> methods of the 
			<b>Graphics</b> class.

## -enum-fields

### -field PixelOffsetModeInvalid

Used internally.

### -field PixelOffsetModeDefault

Equivalent to PixelOffsetModeNone.

### -field PixelOffsetModeHighSpeed

Equivalent to PixelOffsetModeNone.

### -field PixelOffsetModeHighQuality

Equivalent to PixelOffsetModeHalf.

### -field PixelOffsetModeNone

Indicates that pixel centers have integer coordinates.

### -field PixelOffsetModeHalf

Indicates that pixel centers have coordinates that are half way between integer values.

## -remarks

Consider the pixel in the upper-left corner of an image with address (0, 0). With <b>PixelOffsetModeNone</b>, the pixel covers the area between 
				–0.5 and 0.5 in both the x and y directions; that is, the pixel center is at (0, 0). With <b>PixelOffsetModeHalf</b>, the pixel covers the area between 0 and 1 in both the x and y directions; that is, the pixel center is at (0.5, 0.5).

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getpixeloffsetmode">Graphics::GetPixelOffsetMode</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setpixeloffsetmode">Graphics::SetPixelOffsetMode</a>