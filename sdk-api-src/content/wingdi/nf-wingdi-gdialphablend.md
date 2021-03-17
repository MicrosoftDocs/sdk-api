---
UID: NF:wingdi.GdiAlphaBlend
title: GdiAlphaBlend function (wingdi.h)
description: The GdiAlphaBlend function displays bitmaps that have transparent or semitransparent pixels.
helpviewer_keywords: ["GdiAlphaBlend","GdiAlphaBlend function [Windows GDI]","gdi.gdialphablend","wingdi/GdiAlphaBlend"]
old-location: gdi\gdialphablend.htm
tech.root: gdi
ms.assetid: 703d2a6a-0f3f-4f8f-90bd-e1e821dfbcde
ms.date: 12/05/2018
ms.keywords: GdiAlphaBlend, GdiAlphaBlend function [Windows GDI], gdi.gdialphablend, wingdi/GdiAlphaBlend
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
 - GdiAlphaBlend
 - wingdi/GdiAlphaBlend
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GdiAlphaBlend
---

# GdiAlphaBlend function


## -description

The <b>GdiAlphaBlend</b> function displays bitmaps that have transparent or semitransparent pixels.

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

The x-coordinate, in logical units, of the upper-left corner of the source rectangle.

### -param yoriginSrc [in]

The y-coordinate, in logical units, of the upper-left corner of the source rectangle.

### -param wSrc [in]

The width, in logical units, of the source rectangle.

### -param hSrc [in]

The height, in logical units, of the source rectangle.

### -param ftn [in]

The alpha-blending function for source and destination bitmaps, a global alpha value to be applied to the entire source bitmap, and format information for the source bitmap. The source and destination blend functions are currently limited to AC_SRC_OVER. See the <a href="/windows/desktop/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a> and <a href="/windows/desktop/api/wingdi/ns-wingdi-emralphablend">EMRALPHABLEND</a> structures.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.

This function can return the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the input parameters is invalid.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  This function is the same as <a href="/windows/desktop/api/wingdi/nf-wingdi-alphablend">AlphaBlend</a>.</div>
<div> </div>
If the source rectangle and destination rectangle are not the same size, the source bitmap is stretched to match the destination rectangle. If the <a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a> function is used, the <i>iStretchMode</i> value is automatically converted to COLORONCOLOR for this function (that is, BLACKONWHITE, WHITEONBLACK, and HALFTONE are changed to COLORONCOLOR).

The destination coordinates are transformed by using the transformation currently specified for the destination device context. The source coordinates are transformed by using the transformation currently specified for the source device context.

An error occurs (and the function returns <b>FALSE</b>) if the source device context identifies an enhanced metafile device context.

If destination and source bitmaps do not have the same color format, <b>GdiAlphaBlend</b> converts the source bitmap to match the destination bitmap.

<b>GdiAlphaBlend</b> does not support mirroring. If either the width or height of the source or destination is negative, this call will fail.

When rendering to a printer, first call <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> with SHADEBLENDCAPS to determine if the printer supports blending with <b>GdiAlphaBlend</b>. Note that, for a display DC, all blending operations are supported and these flags represent whether the operations are accelerated.

If the source and destination are the same surface, that is, they are both the screen or the same memory bitmap and the source and destination rectangles overlap, an error occurs and the function returns <b>FALSE</b>.

The source rectangle must lie completely within the source surface, otherwise an error occurs and the function returns <b>FALSE</b>.

<b>GdiAlphaBlend</b> fails if the width or height of the source or destination is negative.

The <b>SourceConstantAlpha</b> member of <a href="/windows/desktop/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a> specifies an alpha transparency value to be used on the entire source bitmap. The <b>SourceConstantAlpha</b> value is combined with any per-pixel alpha values. If <b>SourceConstantAlpha</b> is 0, it is assumed that the image is transparent. Set the <b>SourceConstantAlpha</b> value to 255 (which indicates that the image is opaque) when you only want to use per-pixel alpha values.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-blendfunction">BLENDFUNCTION</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-emralphablend">EMRALPHABLEND</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a>