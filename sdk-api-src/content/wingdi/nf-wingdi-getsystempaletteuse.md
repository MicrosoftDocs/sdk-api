---
UID: NF:wingdi.GetSystemPaletteUse
title: GetSystemPaletteUse function (wingdi.h)
description: The GetSystemPaletteUse function retrieves the current state of the system (physical) palette for the specified device context (DC).
helpviewer_keywords: ["GetSystemPaletteUse","GetSystemPaletteUse function [Windows GDI]","_win32_GetSystemPaletteUse","gdi.getsystempaletteuse","wingdi/GetSystemPaletteUse"]
old-location: gdi\getsystempaletteuse.htm
tech.root: gdi
ms.assetid: 0a9e7906-2f81-4fda-b03d-86feb0755327
ms.date: 12/05/2018
ms.keywords: GetSystemPaletteUse, GetSystemPaletteUse function [Windows GDI], _win32_GetSystemPaletteUse, gdi.getsystempaletteuse, wingdi/GetSystemPaletteUse
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
 - GetSystemPaletteUse
 - wingdi/GetSystemPaletteUse
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
 - GetSystemPaletteUse
---

# GetSystemPaletteUse function


## -description

The <b>GetSystemPaletteUse</b> function retrieves the current state of the system (physical) palette for the specified device context (DC).

## -parameters

### -param hdc [in]

A handle to the device context.

## -returns

If the function succeeds, the return value is the current state of the system palette. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>SYSPAL_NOSTATIC</td>
<td>The system palette contains no static colors except black and white.</td>
</tr>
<tr>
<td>SYSPAL_STATIC</td>
<td>The system palette contains static colors that will not change when an application realizes its logical palette.</td>
</tr>
<tr>
<td>SYSPAL_ERROR</td>
<td>The given device context is invalid or does not support a color palette.</td>
</tr>
</table>

## -remarks

By default, the system palette contains 20 static colors that are not changed when an application realizes its logical palette. An application can gain access to most of these colors by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-setsystempaletteuse">SetSystemPaletteUse</a> function.

The device context identified by the <i>hdc</i> parameter must represent a device that supports color palettes.

An application can determine whether a device supports color palettes by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

## -see-also

<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setsystempaletteuse">SetSystemPaletteUse</a>