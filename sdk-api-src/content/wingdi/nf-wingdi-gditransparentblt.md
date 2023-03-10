---
UID: NF:wingdi.GdiTransparentBlt
title: GdiTransparentBlt function (wingdi.h)
description: The GdiTransparentBlt function performs a bit-block transfer of the color data corresponding to a rectangle of pixels from the specified source device context into a destination device context.
helpviewer_keywords: ["GdiTransparentBlt","GdiTransparentBlt function [Windows GDI]","gdi.gditransparentblt","wingdi/GdiTransparentBlt"]
old-location: gdi\gditransparentblt.htm
tech.root: gdi
ms.assetid: 82f6db79-f364-480a-ad9d-acf2ad94a295
ms.date: 12/05/2018
ms.keywords: GdiTransparentBlt, GdiTransparentBlt function [Windows GDI], gdi.gditransparentblt, wingdi/GdiTransparentBlt
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GdiTransparentBlt
 - wingdi/GdiTransparentBlt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GdiTransparentBlt
---

# GdiTransparentBlt function


## -description

The <b>GdiTransparentBlt</b> function performs a bit-block transfer of the color data corresponding to a rectangle of pixels from the specified source device context into a destination device context.
<div class="alert"><b>Note</b>  This function is the same as <a href="/windows/desktop/api/wingdi/nf-wingdi-transparentblt">TransparentBlt</a>.</div><div> </div>

## -parameters

### -param hdcDest [in]

A handle to the destination device context.

### -param xoriginDest [in]

The x-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param yoriginDest [in]

The y-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param wDest [in]

The width, in logical units, of the destination rectangle.

### -param hDest [in]

The height, in logical units, of the destination rectangle.

### -param hdcSrc [in]

A handle to the source device context.

### -param xoriginSrc [in]

The x-coordinate, in logical units, of the source rectangle.

### -param yoriginSrc [in]

The y-coordinate, in logical units, of the source rectangle.

### -param wSrc [in]

The width, in logical units, of the source rectangle.

### -param hSrc [in]

The height, in logical units, of the source rectangle.

### -param crTransparent [in]

The RGB color in the source bitmap to treat as transparent.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.

## -remarks

The <b>GdiTransparentBlt</b> function works with compatible bitmaps (DDBs).

The <a href="/windows/desktop/api/wingdi/nf-wingdi-transparentblt">GdiTransparentBlt</a> function supports all formats of source bitmaps. However, for 32 bpp bitmaps, it just copies the alpha value over. Use <a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a> to specify 32 bits-per-pixel bitmaps with transparency.

If the source and destination rectangles are not the same size, the source bitmap is stretched to match the destination rectangle. When the <a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a> function is used, the <i>iStretchMode</i> modes of BLACKONWHITE and WHITEONBLACK are converted to COLORONCOLOR for the <b>GdiTransparentBlt</b> function.

The destination device context specifies the transformation type for the destination coordinates. The source device context specifies the transformation type for the source coordinates.

<b>GdiTransparentBlt</b> does not mirror a bitmap if either the width or height, of either the source or destination, is negative.

When used in a multiple monitor system, both <i>hdcSrc</i> and <i>hdcDest</i> must refer to the same device or the function will fail. To transfer data between DCs for different devices, convert the memory bitmap to a DIB by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>. To display the DIB to the second device, call <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>