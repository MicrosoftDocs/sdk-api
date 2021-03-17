---
UID: NF:wingdi.RealizePalette
title: RealizePalette function (wingdi.h)
description: The RealizePalette function maps palette entries from the current logical palette to the system palette.
helpviewer_keywords: ["RealizePalette","RealizePalette function [Windows GDI]","_win32_RealizePalette","gdi.realizepalette","wingdi/RealizePalette"]
old-location: gdi\realizepalette.htm
tech.root: gdi
ms.assetid: 1c744ad2-09bc-455f-bc3c-9a2583b57a30
ms.date: 12/05/2018
ms.keywords: RealizePalette, RealizePalette function [Windows GDI], _win32_RealizePalette, gdi.realizepalette, wingdi/RealizePalette
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
 - RealizePalette
 - wingdi/RealizePalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-DC-l1-2-0.dll
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - RealizePalette
---

# RealizePalette function


## -description

The <b>RealizePalette</b> function maps palette entries from the current logical palette to the system palette.

## -parameters

### -param hdc [in]

A handle to the device context into which a logical palette has been selected.

## -returns

If the function succeeds, the return value is the number of entries in the logical palette mapped to the system palette.

If the function fails, the return value is GDI_ERROR.

## -remarks

An application can determine whether a device supports palette operations by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

The <b>RealizePalette</b> function modifies the palette for the device associated with the specified device context. If the device context is a memory DC, the color table for the bitmap selected into the DC is modified. If the device context is a display DC, the physical palette for that device is modified.

A logical palette is a buffer between color-intensive applications and the system, allowing these applications to use as many colors as needed without interfering with colors displayed by other windows.

When an application's window has the focus and it calls the <b>RealizePalette</b> function, the system attempts to realize as many of the requested colors as possible. The same is also true for applications with inactive windows.

## -see-also

<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpalette">CreatePalette</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectpalette">SelectPalette</a>