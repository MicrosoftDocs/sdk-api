---
UID: NF:wingdi.SelectPalette
title: SelectPalette function (wingdi.h)
description: The SelectPalette function selects the specified logical palette into a device context.
helpviewer_keywords: ["SelectPalette","SelectPalette function [Windows GDI]","_win32_SelectPalette","gdi.selectpalette","wingdi/SelectPalette"]
old-location: gdi\selectpalette.htm
tech.root: gdi
ms.assetid: 1fc3356f-6fa3-444f-b224-b953acd2394b
ms.date: 12/05/2018
ms.keywords: SelectPalette, SelectPalette function [Windows GDI], _win32_SelectPalette, gdi.selectpalette, wingdi/SelectPalette
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
 - SelectPalette
 - wingdi/SelectPalette
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
 - SelectPalette
---

# SelectPalette function


## -description

The <b>SelectPalette</b> function selects the specified logical palette into a device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param hPal [in]

A handle to the logical palette to be selected.

### -param bForceBkgd [in]

Specifies whether the logical palette is forced to be a background palette. If this value is <b>TRUE</b>, the <a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a> function causes the logical palette to be mapped to the colors already in the physical palette in the best possible way. This is always done, even if the window for which the palette is realized belongs to a thread without active focus.

If this value is <b>FALSE</b>, <a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a> causes the logical palette to be copied into the device palette when the application is in the foreground. (If the <i>hdc</i> parameter is a memory device context, this parameter is ignored.)

## -returns

If the function succeeds, the return value is a handle to the device context's previous logical palette.

If the function fails, the return value is <b>NULL</b>.

## -remarks

An application can determine whether a device supports palette operations by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

An application can select a logical palette into more than one device context only if device contexts are compatible. Otherwise <b>SelectPalette</b> fails. To create a device context that is compatible with another device context, call <a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc">CreateCompatibleDC</a> with the first device context as the parameter. If a logical palette is selected into more than one device context, changes to the logical palette will affect all device contexts for which it is selected.

An application might call the <b>SelectPalette</b> function with the <i>bForceBackground</i> parameter set to <b>TRUE</b> if the child windows of a top-level window each realize their own palettes. However, only the child window that needs to realize its palette must set <i>bForceBackground</i> to <b>TRUE</b>; other child windows must set this value to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc">CreateCompatibleDC</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpalette">CreatePalette</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-realizepalette">RealizePalette</a>