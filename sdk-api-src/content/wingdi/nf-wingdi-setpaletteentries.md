---
UID: NF:wingdi.SetPaletteEntries
title: SetPaletteEntries function (wingdi.h)
description: The SetPaletteEntries function sets RGB (red, green, blue) color values and flags in a range of entries in a logical palette.
helpviewer_keywords: ["SetPaletteEntries","SetPaletteEntries function [Windows GDI]","_win32_SetPaletteEntries","gdi.setpaletteentries","wingdi/SetPaletteEntries"]
old-location: gdi\setpaletteentries.htm
tech.root: gdi
ms.assetid: df38f482-75ba-4800-8b26-92204c63255e
ms.date: 12/05/2018
ms.keywords: SetPaletteEntries, SetPaletteEntries function [Windows GDI], _win32_SetPaletteEntries, gdi.setpaletteentries, wingdi/SetPaletteEntries
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
 - SetPaletteEntries
 - wingdi/SetPaletteEntries
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
 - SetPaletteEntries
---

# SetPaletteEntries function


## -description

The <b>SetPaletteEntries</b> function sets RGB (red, green, blue) color values and flags in a range of entries in a logical palette.

## -parameters

### -param hpal [in]

A handle to the logical palette.

### -param iStart [in]

The first logical-palette entry to be set.

### -param cEntries [in]

The number of logical-palette entries to be set.

### -param pPalEntries [in]

A pointer to the first member of an array of <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures containing the RGB values and flags.

## -returns

If the function succeeds, the return value is the number of entries that were set in the logical palette.

If the function fails, the return value is zero.

## -remarks

An application can determine whether a device supports palette operations by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

Even if a logical palette has been selected and realized, changes to the palette do not affect the physical palette in the surface. <a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a> must be called again to set the new logical palette into the surface.

## -see-also

<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getpaletteentries">GetPaletteEntries</a>



<a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a>