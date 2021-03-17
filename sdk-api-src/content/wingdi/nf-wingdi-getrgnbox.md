---
UID: NF:wingdi.GetRgnBox
title: GetRgnBox function (wingdi.h)
description: The GetRgnBox function retrieves the bounding rectangle of the specified region.
helpviewer_keywords: ["GetRgnBox","GetRgnBox function [Windows GDI]","_win32_GetRgnBox","gdi.getrgnbox","wingdi/GetRgnBox"]
old-location: gdi\getrgnbox.htm
tech.root: gdi
ms.assetid: 42d06f7f-1bf3-418f-a3b9-c009cf2de10b
ms.date: 12/05/2018
ms.keywords: GetRgnBox, GetRgnBox function [Windows GDI], _win32_GetRgnBox, gdi.getrgnbox, wingdi/GetRgnBox
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
 - GetRgnBox
 - wingdi/GetRgnBox
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-rgn-l1-1-0.dll
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
 - GDI32Full.dll
api_name:
 - GetRgnBox
---

# GetRgnBox function


## -description

The <b>GetRgnBox</b> function retrieves the bounding rectangle of the specified region.

## -parameters

### -param hrgn [in]

A handle to the region.

### -param lprc [out]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the bounding rectangle in logical units.

## -returns

The return value specifies the region's complexity. It can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>NULLREGION</td>
<td>Region is empty.</td>
</tr>
<tr>
<td>SIMPLEREGION</td>
<td>Region is a single rectangle.</td>
</tr>
<tr>
<td>COMPLEXREGION</td>
<td>Region is more than a single rectangle.</td>
</tr>
</table>
 

If the <i>hrgn</i> parameter does not identify a valid region, the return value is zero.

## -see-also

<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>