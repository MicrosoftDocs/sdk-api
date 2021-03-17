---
UID: NF:wingdi.AnimatePalette
title: AnimatePalette function (wingdi.h)
description: The AnimatePalette function replaces entries in the specified logical palette.
helpviewer_keywords: ["AnimatePalette","AnimatePalette function [Windows GDI]","_win32_AnimatePalette","gdi.animatepalette","wingdi/AnimatePalette"]
old-location: gdi\animatepalette.htm
tech.root: gdi
ms.assetid: 65dd45e2-39a4-4a94-bd14-b0c8e4a609a3
ms.date: 12/05/2018
ms.keywords: AnimatePalette, AnimatePalette function [Windows GDI], _win32_AnimatePalette, gdi.animatepalette, wingdi/AnimatePalette
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
 - AnimatePalette
 - wingdi/AnimatePalette
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
 - AnimatePalette
---

# AnimatePalette function


## -description

The <b>AnimatePalette</b> function replaces entries in the specified logical palette.

## -parameters

### -param hPal [in]

A handle to the logical palette.

### -param iStartIndex [in]

The first logical palette entry to be replaced.

### -param cEntries [in]

The number of entries to be replaced.

### -param ppe [in]

A pointer to the first member in an array of <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures used to replace the current entries.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

An application can determine whether a device supports palette operations by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

The <b>AnimatePalette</b> function only changes entries with the PC_RESERVED flag set in the corresponding <b>palPalEntry</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logpalette">LOGPALETTE</a> structure.

If the given palette is associated with the active window, the colors in the palette are replaced immediately.

## -see-also

<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpalette">CreatePalette</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logpalette">LOGPALETTE</a>



<a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a>