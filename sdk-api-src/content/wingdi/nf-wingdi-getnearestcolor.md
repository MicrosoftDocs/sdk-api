---
UID: NF:wingdi.GetNearestColor
title: GetNearestColor function (wingdi.h)
description: The GetNearestColor function retrieves a color value identifying a color from the system palette that will be displayed when the specified color value is used.
helpviewer_keywords: ["GetNearestColor","GetNearestColor function [Windows GDI]","_win32_GetNearestColor","gdi.getnearestcolor","wingdi/GetNearestColor"]
old-location: gdi\getnearestcolor.htm
tech.root: gdi
ms.assetid: 89e4e19b-47be-442e-8eb4-c867bb78f36a
ms.date: 12/05/2018
ms.keywords: GetNearestColor, GetNearestColor function [Windows GDI], _win32_GetNearestColor, gdi.getnearestcolor, wingdi/GetNearestColor
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
 - GetNearestColor
 - wingdi/GetNearestColor
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
 - GetNearestColor
---

# GetNearestColor function


## -description

The <b>GetNearestColor</b> function retrieves a color value identifying a color from the system palette that will be displayed when the specified color value is used.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param color [in]

A color value that identifies a requested color. To create a <a href="/windows/desktop/gdi/colorref">COLORREF</a> color value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

## -returns

If the function succeeds, the return value identifies a color from the system palette that corresponds to the given color value.

If the function fails, the return value is CLR_INVALID.

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="/windows/desktop/gdi/colors">Colors Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="/previous-versions/dd144903(v=vs.85)">GetNearestPaletteIndex</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>