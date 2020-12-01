---
UID: NF:wingdi.CreateHalftonePalette
title: CreateHalftonePalette function (wingdi.h)
description: The CreateHalftonePalette function creates a halftone palette for the specified device context (DC).
helpviewer_keywords: ["CreateHalftonePalette","CreateHalftonePalette function [Windows GDI]","_win32_CreateHalftonePalette","gdi.createhalftonepalette","wingdi/CreateHalftonePalette"]
old-location: gdi\createhalftonepalette.htm
tech.root: gdi
ms.assetid: ba9dfa0c-98df-4922-acba-d00e9b4b0fb0
ms.date: 12/05/2018
ms.keywords: CreateHalftonePalette, CreateHalftonePalette function [Windows GDI], _win32_CreateHalftonePalette, gdi.createhalftonepalette, wingdi/CreateHalftonePalette
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
 - CreateHalftonePalette
 - wingdi/CreateHalftonePalette
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - CreateHalftonePalette
---

# CreateHalftonePalette function


## -description

The <b>CreateHalftonePalette</b> function creates a halftone palette for the specified device context (DC).

## -parameters

### -param hdc [in]

A handle to the device context.

## -returns

If the function succeeds, the return value is a handle to a logical halftone palette.

If the function fails, the return value is zero.

## -remarks

An application should create a halftone palette when the stretching mode of a device context is set to HALFTONE. The logical halftone palette returned by <b>CreateHalftonePalette</b> should then be selected and realized into the device context before the <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a> function is called.

When you no longer need the palette, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

## -see-also

<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectpalette">SelectPalette</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setstretchbltmode">SetStretchBltMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchblt">StretchBlt</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-stretchdibits">StretchDIBits</a>