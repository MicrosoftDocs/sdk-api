---
UID: NF:wingdi.SetSystemPaletteUse
title: SetSystemPaletteUse function (wingdi.h)
description: The SetSystemPaletteUse function allows an application to specify whether the system palette contains 2 or 20 static colors.
helpviewer_keywords: ["SYSPAL_NOSTATIC","SYSPAL_NOSTATIC256","SYSPAL_STATIC","SetSystemPaletteUse","SetSystemPaletteUse function [Windows GDI]","_win32_SetSystemPaletteUse","gdi.setsystempaletteuse","wingdi/SetSystemPaletteUse"]
old-location: gdi\setsystempaletteuse.htm
tech.root: gdi
ms.assetid: 6ff245d3-1bcc-4778-a595-c1eb16531ad3
ms.date: 12/05/2018
ms.keywords: SYSPAL_NOSTATIC, SYSPAL_NOSTATIC256, SYSPAL_STATIC, SetSystemPaletteUse, SetSystemPaletteUse function [Windows GDI], _win32_SetSystemPaletteUse, gdi.setsystempaletteuse, wingdi/SetSystemPaletteUse
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
 - SetSystemPaletteUse
 - wingdi/SetSystemPaletteUse
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
 - SetSystemPaletteUse
---

# SetSystemPaletteUse function


## -description

The <b>SetSystemPaletteUse</b> function allows an application to specify whether the system palette contains 2 or 20 static colors. The default system palette contains 20 static colors. (Static colors cannot be changed when an application realizes a logical palette.)

## -parameters

### -param hdc [in]

A handle to the device context. This device context must refer to a device that supports color palettes.

### -param use [in]

The new use of the system palette. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYSPAL_NOSTATIC"></a><a id="syspal_nostatic"></a><dl>
<dt><b>SYSPAL_NOSTATIC</b></dt>
</dl>
</td>
<td width="60%">
The system palette contains two static colors (black and white).

</td>
</tr>
<tr>
<td width="40%"><a id="SYSPAL_NOSTATIC256"></a><a id="syspal_nostatic256"></a><dl>
<dt><b>SYSPAL_NOSTATIC256</b></dt>
</dl>
</td>
<td width="60%">
The system palette contains no static colors.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSPAL_STATIC"></a><a id="syspal_static"></a><dl>
<dt><b>SYSPAL_STATIC</b></dt>
</dl>
</td>
<td width="60%">
The system palette contains static colors that will not change when an application realizes its logical palette.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the previous system palette. It can be either SYSPAL_NOSTATIC, SYSPAL_NOSTATIC256, or SYSPAL_STATIC.

If the function fails, the return value is SYSPAL_ERROR.

## -remarks

An application can determine whether a device supports palette operations by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

When an application window moves to the foreground and the SYSPAL_NOSTATIC value is set, the application must call the <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> function to save the current system colors setting. It must also call <a href="/windows/desktop/api/winuser/nf-winuser-setsyscolors">SetSysColors</a> to set reasonable values using only black and white. When the application returns to the background or terminates, the previous system colors must be restored.

If the function returns SYSPAL_ERROR, the specified device context is invalid or does not support color palettes.

An application must call this function only when its window is maximized and has the input focus.

If an application calls <b>SetSystemPaletteUse</b> with <i>uUsage</i> set to SYSPAL_NOSTATIC, the system continues to set aside two entries in the system palette for pure white and pure black, respectively.

After calling this function with <i>uUsage</i> set to SYSPAL_NOSTATIC, an application must take the following steps:

<ol>
<li>Realize the logical palette.</li>
<li>Call the <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a> function to save the current system-color settings.</li>
<li>Call the <a href="/windows/desktop/api/winuser/nf-winuser-setsyscolors">SetSysColors</a> function to set the system colors to reasonable values using black and white. For example, adjacent or overlapping items (such as window frames and borders) should be set to black and white, respectively.</li>
<li>Send the <a href="/windows/desktop/gdi/wm-syscolorchange">WM_SYSCOLORCHANGE</a> message to other top-level windows to allow them to be redrawn with the new system colors.</li>
</ol>
When the application's window loses focus or closes, the application must perform the following steps:

<ol>
<li>Call <b>SetSystemPaletteUse</b> with the <i>uUsage</i> parameter set to SYSPAL_STATIC.</li>
<li>Realize the logical palette.</li>
<li>Restore the system colors to their previous values.</li>
<li>Send the <a href="/windows/desktop/gdi/wm-syscolorchange">WM_SYSCOLORCHANGE</a> message.</li>
</ol>

## -see-also

<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getsyscolor">GetSysColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getsystempaletteuse">GetSystemPaletteUse</a>



<a href="/windows/desktop/api/winuser/nf-winuser-setsyscolors">SetSysColors</a>