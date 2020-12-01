---
UID: NF:wingdi.GetPaletteEntries
title: GetPaletteEntries function (wingdi.h)
description: The GetPaletteEntries function retrieves a specified range of palette entries from the given logical palette.
helpviewer_keywords: ["GetPaletteEntries","GetPaletteEntries function [Windows GDI]","_win32_GetPaletteEntries","gdi.getpaletteentries","wingdi/GetPaletteEntries"]
old-location: gdi\getpaletteentries.htm
tech.root: gdi
ms.assetid: 5e72e881-32e1-458e-a09e-91fa13abe178
ms.date: 12/05/2018
ms.keywords: GetPaletteEntries, GetPaletteEntries function [Windows GDI], _win32_GetPaletteEntries, gdi.getpaletteentries, wingdi/GetPaletteEntries
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
 - GetPaletteEntries
 - wingdi/GetPaletteEntries
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
 - GetPaletteEntries
---

# GetPaletteEntries function


## -description

The <b>GetPaletteEntries</b> function retrieves a specified range of palette entries from the given logical palette.

## -parameters

### -param hpal [in]

A handle to the logical palette.

### -param iStart [in]

The first entry in the logical palette to be retrieved.

### -param cEntries [in]

The number of entries in the logical palette to be retrieved.

### -param pPalEntries [out]

A pointer to an array of <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures to receive the palette entries. The array must contain at least as many structures as specified by the <i>nEntries</i> parameter.

## -returns

If the function succeeds and the handle to the logical palette is a valid pointer (not <b>NULL</b>), the return value is the number of entries retrieved from the logical palette. If the function succeeds and handle to the logical palette is <b>NULL</b>, the return value is the number of entries in the given palette.

If the function fails, the return value is zero.

## -remarks

An application can determine whether a device supports palette operations by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

If the <i>nEntries</i> parameter specifies more entries than exist in the palette, the remaining members of the <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structure are not altered.

## -see-also

<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getsystempaletteentries">GetSystemPaletteEntries</a>



<a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpaletteentries">SetPaletteEntries</a>