---
UID: NF:wingdi.CreateCompatibleBitmap
title: CreateCompatibleBitmap function (wingdi.h)
description: The CreateCompatibleBitmap function creates a bitmap compatible with the device that is associated with the specified device context.
helpviewer_keywords: ["CreateCompatibleBitmap","CreateCompatibleBitmap function [Windows GDI]","_win32_CreateCompatibleBitmap","gdi.createcompatiblebitmap","wingdi/CreateCompatibleBitmap"]
old-location: gdi\createcompatiblebitmap.htm
tech.root: gdi
ms.assetid: d2866beb-ff7a-4390-8651-e7bf458ddf88
ms.date: 12/05/2018
ms.keywords: CreateCompatibleBitmap, CreateCompatibleBitmap function [Windows GDI], _win32_CreateCompatibleBitmap, gdi.createcompatiblebitmap, wingdi/CreateCompatibleBitmap
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
 - CreateCompatibleBitmap
 - wingdi/CreateCompatibleBitmap
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
 - CreateCompatibleBitmap
---

# CreateCompatibleBitmap function


## -description

The <b>CreateCompatibleBitmap</b> function creates a bitmap compatible with the device that is associated with the specified device context.

## -parameters

### -param hdc [in]

A handle to a device context.

### -param cx [in]

The bitmap width, in pixels.

### -param cy [in]

The bitmap height, in pixels.

## -returns

If the function succeeds, the return value is a handle to the compatible bitmap (DDB).

If the function fails, the return value is <b>NULL</b>.

## -remarks

The color format of the bitmap created by the <b>CreateCompatibleBitmap</b> function matches the color format of the device identified by the <i>hdc</i> parameter. This bitmap can be selected into any memory device context that is compatible with the original device.

Because memory device contexts allow both color and monochrome bitmaps, the format of the bitmap returned by the <b>CreateCompatibleBitmap</b> function differs when the specified device context is a memory device context. However, a compatible bitmap that was created for a nonmemory device context always possesses the same color format and uses the same color palette as the specified device context.

Note: When a memory device context is created, it initially has a 1-by-1 monochrome bitmap selected into it. If this memory device context is used in <b>CreateCompatibleBitmap</b>, the bitmap that is created is a <i>monochrome</i> bitmap. To create a color bitmap, use the <b>HDC</b> that was used to create the memory device context, as shown in the following code:


```cpp

    HDC memDC = CreateCompatibleDC ( hDC );
    HBITMAP memBM = CreateCompatibleBitmap ( hDC, nWidth, nHeight );
    SelectObject ( memDC, memBM );

```


If an application sets the <i>nWidth</i> or <i>nHeight</i> parameters to zero, <b>CreateCompatibleBitmap</b> returns the handle to a 1-by-1 pixel, monochrome bitmap.

If a DIB section, which is a bitmap created by the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a> function, is selected into the device context identified by the <i>hdc</i> parameter, <b>CreateCompatibleBitmap</b> creates a DIB section.

When you no longer need the bitmap, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.


#### Examples

For an example, see <a href="/windows/desktop/gdi/scaling-an-image">Scaling an Image</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>