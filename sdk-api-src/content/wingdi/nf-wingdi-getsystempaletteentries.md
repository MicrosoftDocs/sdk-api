---
UID: NF:wingdi.GetSystemPaletteEntries
title: GetSystemPaletteEntries function (wingdi.h)
description: The GetSystemPaletteEntries function retrieves a range of palette entries from the system palette that is associated with the specified device context (DC).
helpviewer_keywords: ["GetSystemPaletteEntries","GetSystemPaletteEntries function [Windows GDI]","_win32_GetSystemPaletteEntries","gdi.getsystempaletteentries","wingdi/GetSystemPaletteEntries"]
old-location: gdi\getsystempaletteentries.htm
tech.root: gdi
ms.assetid: 67bb0adf-ae7f-48d5-bc62-82ece45aeee6
ms.date: 12/05/2018
ms.keywords: GetSystemPaletteEntries, GetSystemPaletteEntries function [Windows GDI], _win32_GetSystemPaletteEntries, gdi.getsystempaletteentries, wingdi/GetSystemPaletteEntries
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
 - GetSystemPaletteEntries
 - wingdi/GetSystemPaletteEntries
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
 - GetSystemPaletteEntries
---

# GetSystemPaletteEntries function


## -description

The <b>GetSystemPaletteEntries</b> function retrieves a range of palette entries from the system palette that is associated with the specified device context (DC).

## -parameters

### -param hdc [in]

A handle to the device context.

### -param iStart [in]

The first entry to be retrieved from the system palette.

### -param cEntries [in]

The number of entries to be retrieved from the system palette.

### -param pPalEntries [out]

A pointer to an array of <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures to receive the palette entries. The array must contain at least as many structures as specified by the <i>cEntries</i> parameter. If this parameter is <b>NULL</b>, the function returns the total number of entries in the palette.

## -returns

If the function succeeds, the return value is the number of entries retrieved from the palette.

If the function fails, the return value is zero.

## -remarks

An application can determine whether a device supports palette operations by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

## -see-also

<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getpaletteentries">GetPaletteEntries</a>



<a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a>