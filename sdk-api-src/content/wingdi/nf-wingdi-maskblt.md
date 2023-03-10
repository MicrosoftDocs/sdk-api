---
UID: NF:wingdi.MaskBlt
title: MaskBlt function (wingdi.h)
description: The MaskBlt function combines the color data for the source and destination bitmaps using the specified mask and raster operation.
helpviewer_keywords: ["MaskBlt","MaskBlt function [Windows GDI]","_win32_MaskBlt","gdi.maskblt","wingdi/MaskBlt"]
old-location: gdi\maskblt.htm
tech.root: gdi
ms.assetid: 9fd6f0ce-a802-428d-9be5-a66afe39e9b7
ms.date: 12/05/2018
ms.keywords: MaskBlt, MaskBlt function [Windows GDI], _win32_MaskBlt, gdi.maskblt, wingdi/MaskBlt
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
 - MaskBlt
 - wingdi/MaskBlt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - MaskBlt
---

# MaskBlt function


## -description

The <b>MaskBlt</b> function combines the color data for the source and destination bitmaps using the specified mask and raster operation.

## -parameters

### -param hdcDest [in]

A handle to the destination device context.

### -param xDest [in]

The x-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param yDest [in]

The y-coordinate, in logical units, of the upper-left corner of the destination rectangle.

### -param width [in]

The width, in logical units, of the destination rectangle and source bitmap.

### -param height [in]

The height, in logical units, of the destination rectangle and source bitmap.

### -param hdcSrc [in]

A handle to the device context from which the bitmap is to be copied. It must be zero if the <i>dwRop</i> parameter specifies a raster operation that does not include a source.

### -param xSrc [in]

The x-coordinate, in logical units, of the upper-left corner of the source bitmap.

### -param ySrc [in]

The y-coordinate, in logical units, of the upper-left corner of the source bitmap.

### -param hbmMask [in]

A handle to the monochrome mask bitmap combined with the color bitmap in the source device context.

### -param xMask [in]

The horizontal pixel offset for the mask bitmap specified by the <i>hbmMask</i> parameter.

### -param yMask [in]

The vertical pixel offset for the mask bitmap specified by the <i>hbmMask</i> parameter.

### -param rop [in]

The foreground and background ternary raster operation codes (ROPs) that the function uses to control the combination of source and destination data. The background raster operation code is stored in the high-order byte of the high-order word of this value; the foreground raster operation code is stored in the low-order byte of the high-order word of this value; the low-order word of this value is ignored, and should be zero. The macro <a href="/windows/desktop/api/wingdi/nf-wingdi-makerop4">MAKEROP4</a> creates such combinations of foreground and background raster operation codes.

For a discussion of foreground and background in the context of this function, see the following Remarks section.

For a list of common raster operation codes (ROPs), see the <a href="/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a> function. Note that the CAPTUREBLT ROP generally cannot be used for printing device contexts.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>MaskBlt</b> function uses device-dependent bitmaps.

A value of 1 in the mask specified by <i>hbmMask</i> indicates that the foreground raster operation code specified by <i>dwRop</i> should be applied at that location. A value of 0 in the mask indicates that the background raster operation code specified by <i>dwRop</i> should be applied at that location.

If the raster operations require a source, the mask rectangle must cover the source rectangle. If it does not, the function will fail. If the raster operations do not require a source, the mask rectangle must cover the destination rectangle. If it does not, the function will fail.

If a rotation or shear transformation is in effect for the source device context when this function is called, an error occurs. However, other types of transformation are allowed.

If the color formats of the source, pattern, and destination bitmaps differ, this function converts the pattern or source format, or both, to match the destination format.

If the mask bitmap is not a monochrome bitmap, an error occurs.

When an enhanced metafile is being recorded, an error occurs (and the function returns <b>FALSE</b>) if the source device context identifies an enhanced-metafile device context.

Not all devices support the <b>MaskBlt</b> function. An application should call the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function with the <i>nIndex</i> parameter as RC_BITBLT to determine whether a device supports this function.

If no mask bitmap is supplied, this function behaves exactly like <a href="/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a>, using the foreground raster operation code.

<b>ICM:</b> No color management is performed when blits occur.

When used in a multiple monitor system, both <i>hdcSrc</i> and <i>hdcDest</i> must refer to the same device or the function will fail. To transfer data between DCs for different devices, convert the memory bitmap (compatible bitmap, or DDB) to a DIB by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>. To display the DIB to the second device, call <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-plgblt">PlgBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>