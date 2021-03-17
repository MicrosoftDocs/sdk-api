---
UID: NE:gdiplusenums.SmoothingMode
title: SmoothingMode (gdiplusenums.h)
description: The SmoothingMode enumeration specifies the type of smoothing (antialiasing) that is applied to lines and curves. This enumeration is used by the Graphics::GetSmoothingMode and Graphics::SetSmoothingMode methods of the Graphics class.
helpviewer_keywords: ["SmoothingMode","SmoothingMode enumeration [GDI+]","SmoothingModeAntiAlias","SmoothingModeAntiAlias8x4","SmoothingModeAntiAlias8x8","SmoothingModeDefault","SmoothingModeHighQuality","SmoothingModeHighSpeed","SmoothingModeInvalid","SmoothingModeNone","_gdiplus_ENUM_SmoothingMode","gdiplus._gdiplus_ENUM_SmoothingMode","gdiplusenums/SmoothingMode","gdiplusenums/SmoothingModeAntiAlias","gdiplusenums/SmoothingModeAntiAlias8x4","gdiplusenums/SmoothingModeAntiAlias8x8","gdiplusenums/SmoothingModeDefault","gdiplusenums/SmoothingModeHighQuality","gdiplusenums/SmoothingModeHighSpeed","gdiplusenums/SmoothingModeInvalid","gdiplusenums/SmoothingModeNone"]
old-location: gdiplus\_gdiplus_ENUM_SmoothingMode.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\smoothingmode.htm
ms.date: 12/05/2018
ms.keywords: SmoothingMode, SmoothingMode enumeration [GDI+], SmoothingModeAntiAlias, SmoothingModeAntiAlias8x4, SmoothingModeAntiAlias8x8, SmoothingModeDefault, SmoothingModeHighQuality, SmoothingModeHighSpeed, SmoothingModeInvalid, SmoothingModeNone, _gdiplus_ENUM_SmoothingMode, gdiplus._gdiplus_ENUM_SmoothingMode, gdiplusenums/SmoothingMode, gdiplusenums/SmoothingModeAntiAlias, gdiplusenums/SmoothingModeAntiAlias8x4, gdiplusenums/SmoothingModeAntiAlias8x8, gdiplusenums/SmoothingModeDefault, gdiplusenums/SmoothingModeHighQuality, gdiplusenums/SmoothingModeHighSpeed, gdiplusenums/SmoothingModeInvalid, gdiplusenums/SmoothingModeNone
req.header: gdiplusenums.h
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
 - SmoothingMode
 - gdiplusenums/SmoothingMode
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
 - SmoothingMode
---

# SmoothingMode enumeration


## -description

The <b>SmoothingMode</b> enumeration specifies the type of smoothing (antialiasing) that is applied to lines and curves. This enumeration is used by the <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getsmoothingmode">Graphics::GetSmoothingMode</a> and <a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode">Graphics::SetSmoothingMode</a> methods of the 
			<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> class.

## -enum-fields

### -field SmoothingModeInvalid

Reserved.

### -field SmoothingModeDefault

Specifies that smoothing is not applied.

### -field SmoothingModeHighSpeed

Specifies that smoothing is not applied.

### -field SmoothingModeHighQuality

Specifies that smoothing is applied using an 8 X 4 box filter.

### -field SmoothingModeNone

Specifies that smoothing is not applied.

### -field SmoothingModeAntiAlias

Specifies that smoothing is applied using an 8 X 4 box filter.

### -field SmoothingModeAntiAlias8x4

Specifies that smoothing is applied using an 8 X 4 box filter.

### -field SmoothingModeAntiAlias8x8

Specifies that smoothing is applied using an 8 X 8 box filter.

## -remarks

Smoothing performed by an 8 X 4 box filter gives better results for nearly vertical lines than it does for nearly horizontal lines. Smoothing performed by an 8 X 8 box filter gives equally good results for nearly vertical and nearly horizontal lines. The 8x8 algorithm produces higher quality smoothing but is slower than the 8 X 4 algorithm.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-getsmoothingmode">Graphics::GetSmoothingMode</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode">Graphics::SetSmoothingMode</a>