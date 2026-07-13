---
UID: NF:wingdi.CreateBitmap
title: CreateBitmap function (wingdi.h)
description: The CreateBitmap function creates a bitmap with the specified width, height, and color format (color planes and bits-per-pixel).
helpviewer_keywords: ["CreateBitmap","CreateBitmap function [Windows GDI]","_win32_CreateBitmap","gdi.createbitmap","wingdi/CreateBitmap"]
old-location: gdi\createbitmap.htm
tech.root: gdi
ms.assetid: b52e1baf-6a81-44bc-a061-4d42e6f4ed64
ms.date: 12/05/2018
ms.keywords: CreateBitmap, CreateBitmap function [Windows GDI], _win32_CreateBitmap, gdi.createbitmap, wingdi/CreateBitmap
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
 - CreateBitmap
 - wingdi/CreateBitmap
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
 - CreateBitmap
---

## -description

The <b>CreateBitmap</b> function creates a bitmap with the specified width, height, and color format (color planes and bits-per-pixel).

## -parameters

### -param nWidth [in]

The bitmap width, in pixels.

### -param nHeight [in]

The bitmap height, in pixels.

### -param nPlanes [in]

The number of color planes used by the device.

### -param nBitCount [in]

The number of bits required to identify the color of a single pixel.

### -param lpBits [in]

A pointer to an array of color data used to set the colors in a rectangle of pixels. Each scan line in the rectangle must be word aligned (scan lines that are not word aligned must be padded with zeros). The buffer size expected, *cj*, can be calculated using the formula:

```cpp
cj = (((nWidth * nPlanes * nBitCount + 15) >> 4) << 1) * nHeight;
```

If this parameter is <b>NULL</b>, then the contents of the new bitmap are undefined.

## -returns

If the function succeeds, the return value is a handle to a bitmap.

If the function fails, the return value is <b>NULL</b>.

This function can return the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_BITMAP</b></dt>
</dl>
</td>
<td width="60%">
The calculated size of the bitmap is less than zero.

</td>
</tr>
</table>

## -remarks

The <b>CreateBitmap</b> function creates a device-dependent bitmap.

After a bitmap is created, it can be selected into a device context by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> function. However, the bitmap can only be selected into a device context if the bitmap and the DC have the same format.

The <b>CreateBitmap</b> function can be used to create color bitmaps. However, for performance reasons applications should use <b>CreateBitmap</b> to create monochrome bitmaps and <a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a> to create color bitmaps. Whenever a color bitmap returned from <b>CreateBitmap</b> is selected into a device context, the system checks that the bitmap matches the format of the device context it is being selected into. Because <b>CreateCompatibleBitmap</b> takes a device context, it returns a bitmap that has the same format as the specified device context. Thus, subsequent calls to <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> are faster with a color bitmap from <b>CreateCompatibleBitmap</b> than with a color bitmap returned from <b>CreateBitmap</b>.

If the bitmap is monochrome, zeros represent the foreground color and ones represent the background color for the destination device context.

If an application sets the <i>nWidth</i> or <i>nHeight</i> parameters to zero, <b>CreateBitmap</b> returns the handle to a 1-by-1 pixel, monochrome bitmap.

When you no longer need the bitmap, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmapindirect">CreateBitmapIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibitmap">CreateDIBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getbitmapbits">GetBitmapBits</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbitmapbits">SetBitmapBits</a>
