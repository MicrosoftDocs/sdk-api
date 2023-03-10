---
UID: NF:wingdi.CreatePalette
title: CreatePalette function (wingdi.h)
description: The CreatePalette function creates a logical palette.
helpviewer_keywords: ["CreatePalette","CreatePalette function [Windows GDI]","_win32_CreatePalette","gdi.createpalette","wingdi/CreatePalette"]
old-location: gdi\createpalette.htm
tech.root: gdi
ms.assetid: f3462198-9360-4b77-ac62-9fe21ec666be
ms.date: 12/05/2018
ms.keywords: CreatePalette, CreatePalette function [Windows GDI], _win32_CreatePalette, gdi.createpalette, wingdi/CreatePalette
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
 - CreatePalette
 - wingdi/CreatePalette
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
 - ext-ms-win-gdi-dc-l1-1-0.dll
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - CreatePalette
---

# CreatePalette function


## -description

The <b>CreatePalette</b> function creates a logical palette.

## -parameters

### -param plpal [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-logpalette">LOGPALETTE</a> structure that contains information about the colors in the logical palette.

## -returns

If the function succeeds, the return value is a handle to a logical palette.

If the function fails, the return value is <b>NULL</b>.

## -remarks

An application can determine whether a device supports palette operations by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

Once an application creates a logical palette, it can select that palette into a device context by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectpalette">SelectPalette</a> function. A palette selected into a device context can be realized by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a> function.

When you no longer need the palette, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

## -see-also

<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logpalette">LOGPALETTE</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectpalette">SelectPalette</a>