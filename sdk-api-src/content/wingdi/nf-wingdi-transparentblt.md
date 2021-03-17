---
UID: NF:wingdi.TransparentBlt
title: TransparentBlt function (wingdi.h)
description: The TransparentBlt function performs a bit-block transfer of the color data corresponding to a rectangle of pixels from the specified source device context into a destination device context.
helpviewer_keywords: ["TransparentBlt","TransparentBlt function [Windows GDI]","_win32_TransparentBlt","gdi.transparentblt","wingdi/TransparentBlt"]
old-location: gdi\transparentblt.htm
tech.root: gdi
ms.assetid: 900b2ca3-398d-4128-a1ae-8b4940574327
ms.date: 12/05/2018
ms.keywords: TransparentBlt, TransparentBlt function [Windows GDI], _win32_TransparentBlt, gdi.transparentblt, wingdi/TransparentBlt
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
req.lib: Msimg32.lib
req.dll: Msimg32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TransparentBlt
 - wingdi/TransparentBlt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msimg32.dll
 - ext-ms-win-msimg-draw-l1-1-0.dll
api_name:
 - TransparentBlt
---

# TransparentBlt function


## -description

The <b>TransparentBlt</b> function performs a bit-block transfer of the color data corresponding to a rectangle of pixels from the specified source device context into a destination device context.

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

The <b>TransparentBlt</b> function works with compatible bitmaps (DDBs).

The <b>TransparentBlt</b> function supports all formats of source bitmaps. However, for 32 bpp bitmaps, it just copies the alpha value over. Use <a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a> to specify 32 bits-per-pixel bitmaps with transparency.

If the source and destination rectangles are not the same size, the source bitmap is stretched to match the destination rectangle. When the <a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a> function is used, the <i>iStretchMode</i> modes of BLACKONWHITE and WHITEONBLACK are converted to COLORONCOLOR for the <b>TransparentBlt</b> function.

The destination device context specifies the transformation type for the destination coordinates. The source device context specifies the transformation type for the source coordinates.

<b>TransparentBlt</b> does not mirror a bitmap if either the width or height, of either the source or destination, is negative.

When used in a multiple monitor system, both <i>hdcSrc</i> and <i>hdcDest</i> must refer to the same device or the function will fail. To transfer data between DCs for different devices, convert the memory bitmap to a DIB by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>. To display the DIB to the second device, call <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>