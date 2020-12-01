---
UID: NF:wingdi.SetPixelV
title: SetPixelV function (wingdi.h)
description: The SetPixelV function sets the pixel at the specified coordinates to the closest approximation of the specified color. The point must be in the clipping region and the visible part of the device surface.
helpviewer_keywords: ["SetPixelV","SetPixelV function [Windows GDI]","_win32_SetPixelV","gdi.setpixelv","wingdi/SetPixelV"]
old-location: gdi\setpixelv.htm
tech.root: gdi
ms.assetid: 638f0ffd-3771-4390-b335-0517be5312fd
ms.date: 12/05/2018
ms.keywords: SetPixelV, SetPixelV function [Windows GDI], _win32_SetPixelV, gdi.setpixelv, wingdi/SetPixelV
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
 - SetPixelV
 - wingdi/SetPixelV
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
 - SetPixelV
---

# SetPixelV function


## -description

The <b>SetPixelV</b> function sets the pixel at the specified coordinates to the closest approximation of the specified color. The point must be in the clipping region and the visible part of the device surface.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param x [in]

The x-coordinate, in logical units, of the point to be set.

### -param y [in]

The y-coordinate, in logical units, of the point to be set.

### -param color [in]

The color to be used to paint the point. To create a <a href="/windows/desktop/gdi/colorref">COLORREF</a> color value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Not all devices support the <b>SetPixelV</b> function. For more information, see the description of the RC_BITBLT capability in the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function.

<b>SetPixelV</b> is faster than <a href="/windows/desktop/api/wingdi/nf-wingdi-setpixel">SetPixel</a> because it does not need to return the color value of the point actually painted.

## -see-also

<a href="/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpixel">SetPixel</a>