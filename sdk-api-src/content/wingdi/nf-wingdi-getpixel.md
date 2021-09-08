---
UID: NF:wingdi.GetPixel
title: GetPixel function (wingdi.h)
description: The GetPixel function retrieves the red, green, blue (RGB) color value of the pixel at the specified coordinates.
helpviewer_keywords: ["GetPixel","GetPixel function [Windows GDI]","_win32_GetPixel","gdi.getpixel","wingdi/GetPixel"]
old-location: gdi\getpixel.htm
tech.root: gdi
ms.assetid: 46d17e95-93ce-4a43-b86c-489d6e3afe12
ms.date: 12/05/2018
ms.keywords: GetPixel, GetPixel function [Windows GDI], _win32_GetPixel, gdi.getpixel, wingdi/GetPixel
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
 - GetPixel
 - wingdi/GetPixel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetPixel
---

# GetPixel function


## -description

The <b>GetPixel</b> function retrieves the red, green, blue (RGB) color value of the pixel at the specified coordinates.

## -parameters

### -param hdc [in]

A handle to the [device context](/windows/win32/gdi/device-contexts).

### -param x [in]

The x-coordinate, in logical units, of the pixel to be examined.

### -param y [in]

The y-coordinate, in logical units, of the pixel to be examined.

## -returns

The return value is the <a href="/windows/desktop/gdi/colorref">COLORREF</a> value that specifies the RGB of the pixel. If the pixel is outside of the current clipping region, the return value is CLR_INVALID (0xFFFFFFFF defined in Wingdi.h).

## -remarks

The pixel must be within the boundaries of the current clipping region.

Not all devices support <b>GetPixel</b>. An application should call <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> to determine whether a specified device supports this function.

A bitmap must be selected within the device context, otherwise, CLR_INVALID is returned on all pixels.

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpixel">SetPixel</a>
