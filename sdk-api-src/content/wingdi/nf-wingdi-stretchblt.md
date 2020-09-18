---
UID: NF:wingdi.StretchBlt
title: StretchBlt function (wingdi.h)
description: The StretchBlt function copies a bitmap from a source rectangle into a destination rectangle, stretching or compressing the bitmap to fit the dimensions of the destination rectangle, if necessary.
helpviewer_keywords: ["StretchBlt","StretchBlt function [Windows GDI]","_win32_StretchBlt","gdi.stretchblt","wingdi/StretchBlt"]
old-location: gdi\stretchblt.htm
tech.root: gdi
ms.assetid: 5130c88e-08e8-4faa-a1cb-a8106c86cea0
ms.date: 12/05/2018
ms.keywords: StretchBlt, StretchBlt function [Windows GDI], _win32_StretchBlt, gdi.stretchblt, wingdi/StretchBlt
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
 - StretchBlt
 - wingdi/StretchBlt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - StretchBlt
---

# StretchBlt function


## -description

The <b>StretchBlt</b> function copies a bitmap from a source rectangle into a destination rectangle, stretching or compressing the bitmap to fit the dimensions of the destination rectangle, if necessary. The system stretches or compresses the bitmap according to the stretching mode currently set in the destination device context.

## -parameters

### -param hdcDest [in]

A handle to the destination device context.

### -param xDest [in]

The x-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param yDest [in]

The y-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param wDest [in]

The width, in logical units, of the destination rectangle.

### -param hDest [in]

The height, in logical units, of the destination rectangle.

### -param hdcSrc [in]

A handle to the source device context.

### -param xSrc [in]

The x-coordinate, in logical units, of the upper-left corner of the source rectangle.

### -param ySrc [in]

The y-coordinate, in logical units, of the upper-left corner of the source rectangle.

### -param wSrc [in]

The width, in logical units, of the source rectangle.

### -param hSrc [in]

The height, in logical units, of the source rectangle.

### -param rop [in]

The raster operation to be performed. Raster operation codes define how the system combines colors in output operations that involve a brush, a source bitmap, and a destination bitmap.

See <a href="/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a> for a list of common raster operation codes (ROPs). Note that the CAPTUREBLT ROP generally cannot be used for printing device contexts.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

<b>StretchBlt</b> stretches or compresses the source bitmap in memory and then copies the result to the destination rectangle. This bitmap can be either a compatible bitmap (DDB) or the output from <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>. The color data for pattern or destination pixels is merged after the stretching or compression occurs.

When an enhanced metafile is being recorded, an error occurs (and the function returns <b>FALSE</b>) if the source device context identifies an enhanced-metafile device context.

If the specified raster operation requires a brush, the system uses the brush currently selected into the destination device context.

The destination coordinates are transformed by using the transformation currently specified for the destination device context; the source coordinates are transformed by using the transformation currently specified for the source device context.

If the source transformation has a rotation or shear, an error occurs.

If destination, source, and pattern bitmaps do not have the same color format, <b>StretchBlt</b> converts the source and pattern bitmaps to match the destination bitmap.

If <b>StretchBlt</b> must convert a monochrome bitmap to a color bitmap, it sets white bits (1) to the background color and black bits (0) to the foreground color. To convert a color bitmap to a monochrome bitmap, it sets pixels that match the background color to white (1) and sets all other pixels to black (0). The foreground and background colors of the device context with color are used.

<b>StretchBlt</b> creates a mirror image of a bitmap if the signs of the <i>nWidthSrc</i> and <i>nWidthDest</i> parameters or if the <i>nHeightSrc</i> and <i>nHeightDest</i> parameters differ. If <i>nWidthSrc</i> and <i>nWidthDest</i> have different signs, the function creates a mirror image of the bitmap along the x-axis. If <i>nHeightSrc</i> and <i>nHeightDest</i> have different signs, the function creates a mirror image of the bitmap along the y-axis.

Not all devices support the <b>StretchBlt</b> function. For more information, see the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>.

<b>ICM:</b> No color management is performed when a blit operation occurs.

When used in a multiple monitor system, both <i>hdcSrc</i> and <i>hdcDest</i> must refer to the same device or the function will fail. To transfer data between DCs for different devices, convert the memory bitmap to a DIB by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>. To display the DIB to the second device, call <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>.


#### Examples

For an example, see <a href="/windows/desktop/gdi/scaling-an-image">Scaling an Image</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-maskblt">MaskBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-plgblt">PlgBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>