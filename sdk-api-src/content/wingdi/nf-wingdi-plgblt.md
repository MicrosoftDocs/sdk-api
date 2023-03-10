---
UID: NF:wingdi.PlgBlt
title: PlgBlt function (wingdi.h)
description: The PlgBlt function performs a bit-block transfer of the bits of color data from the specified rectangle in the source device context to the specified parallelogram in the destination device context.
helpviewer_keywords: ["PlgBlt","PlgBlt function [Windows GDI]","_win32_PlgBlt","gdi.plgblt","wingdi/PlgBlt"]
old-location: gdi\plgblt.htm
tech.root: gdi
ms.assetid: 2a56c71b-2e96-418b-8625-a808d76e0c85
ms.date: 12/05/2018
ms.keywords: PlgBlt, PlgBlt function [Windows GDI], _win32_PlgBlt, gdi.plgblt, wingdi/PlgBlt
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
 - PlgBlt
 - wingdi/PlgBlt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - PlgBlt
---

# PlgBlt function


## -description

The <b>PlgBlt</b> function performs a bit-block transfer of the bits of color data from the specified rectangle in the source device context to the specified parallelogram in the destination device context. If the given bitmask handle identifies a valid monochrome bitmap, the function uses this bitmap to mask the bits of color data from the source rectangle.

## -parameters

### -param hdcDest [in]

A handle to the destination device context.

### -param lpPoint [in]

A pointer to an array of three points in logical space that identify three corners of the destination parallelogram. The upper-left corner of the source rectangle is mapped to the first point in this array, the upper-right corner to the second point in this array, and the lower-left corner to the third point. The lower-right corner of the source rectangle is mapped to the implicit fourth point in the parallelogram.

### -param hdcSrc [in]

A handle to the source device context.

### -param xSrc [in]

The x-coordinate, in logical units, of the upper-left corner of the source rectangle.

### -param ySrc [in]

The y-coordinate, in logical units, of the upper-left corner of the source rectangle.

### -param width [in]

The width, in logical units, of the source rectangle.

### -param height [in]

The height, in logical units, of the source rectangle.

### -param hbmMask [in]

A handle to an optional monochrome bitmap that is used to mask the colors of the source rectangle.

### -param xMask [in]

The x-coordinate, in logical units, of the upper-left corner of the monochrome bitmap.

### -param yMask [in]

The y-coordinate, in logical units, of the upper-left corner of the monochrome bitmap.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>PlgBlt</b> function works with device-dependent bitmaps.

The fourth vertex of the parallelogram (D) is defined by treating the first three points (A, B, and C ) as vectors and computing D = B +CA.

If the bitmask exists, a value of one in the mask indicates that the source pixel color should be copied to the destination. A value of zero in the mask indicates that the destination pixel color is not to be changed. If the mask rectangle is smaller than the source and destination rectangles, the function replicates the mask pattern.

Scaling, translation, and reflection transformations are allowed in the source device context; however, rotation and shear transformations are not. If the mask bitmap is not a monochrome bitmap, an error occurs. The stretching mode for the destination device context is used to determine how to stretch or compress the pixels, if that is necessary.

When an enhanced metafile is being recorded, an error occurs if the source device context identifies an enhanced-metafile device context.

The destination coordinates are transformed according to the destination device context; the source coordinates are transformed according to the source device context. If the source transformation has a rotation or shear, an error is returned.

If the destination and source rectangles do not have the same color format, <b>PlgBlt</b> converts the source rectangle to match the destination rectangle.

Not all devices support the <b>PlgBlt</b> function. For more information, see the description of the RC_BITBLT raster capability in the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function.

If the source and destination device contexts represent incompatible devices, <b>PlgBlt</b> returns an error.

When used in a multiple monitor system, both <i>hdcSrc</i> and <i>hdcDest</i> must refer to the same device or the function will fail. To transfer data between DCs for different devices, convert the memory bitmap to a DIB by calling <a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>. To display the DIB to the second device, call <a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-bitblt">BitBlt</a>



<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibits">GetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-maskblt">MaskBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setdibits">SetDIBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>