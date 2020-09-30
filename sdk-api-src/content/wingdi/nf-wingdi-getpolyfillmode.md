---
UID: NF:wingdi.GetPolyFillMode
title: GetPolyFillMode function (wingdi.h)
description: The GetPolyFillMode function retrieves the current polygon fill mode.
helpviewer_keywords: ["GetPolyFillMode","GetPolyFillMode function [Windows GDI]","_win32_GetPolyFillMode","gdi.getpolyfillmode","wingdi/GetPolyFillMode"]
old-location: gdi\getpolyfillmode.htm
tech.root: gdi
ms.assetid: febf96fb-bf2e-4eb2-ab5f-89741a1decad
ms.date: 12/05/2018
ms.keywords: GetPolyFillMode, GetPolyFillMode function [Windows GDI], _win32_GetPolyFillMode, gdi.getpolyfillmode, wingdi/GetPolyFillMode
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
 - GetPolyFillMode
 - wingdi/GetPolyFillMode
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
 - GetPolyFillMode
---

# GetPolyFillMode function


## -description

The <b>GetPolyFillMode</b> function retrieves the current polygon fill mode.

## -parameters

### -param hdc [in]

Handle to the device context.

## -returns

If the function succeeds, the return value specifies the polygon fill mode, which can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>ALTERNATE</td>
<td>Selects alternate mode (fills area between odd-numbered and even-numbered polygon sides on each scan line).</td>
</tr>
<tr>
<td>WINDING</td>
<td>Selects winding mode (fills any region with a nonzero winding value).</td>
</tr>
</table>
 

If an error occurs, the return value is zero.

## -see-also

<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpolyfillmode">SetPolyFillMode</a>