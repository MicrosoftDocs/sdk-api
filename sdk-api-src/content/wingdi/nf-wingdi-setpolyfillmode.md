---
UID: NF:wingdi.SetPolyFillMode
title: SetPolyFillMode function (wingdi.h)
description: The SetPolyFillMode function sets the polygon fill mode for functions that fill polygons.
helpviewer_keywords: ["ALTERNATE","SetPolyFillMode","SetPolyFillMode function [Windows GDI]","WINDING","_win32_SetPolyFillMode","gdi.setpolyfillmode","wingdi/SetPolyFillMode"]
old-location: gdi\setpolyfillmode.htm
tech.root: gdi
ms.assetid: 233926c4-2658-405d-89b6-05ece844623d
ms.date: 12/05/2018
ms.keywords: ALTERNATE, SetPolyFillMode, SetPolyFillMode function [Windows GDI], WINDING, _win32_SetPolyFillMode, gdi.setpolyfillmode, wingdi/SetPolyFillMode
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
 - SetPolyFillMode
 - wingdi/SetPolyFillMode
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
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetPolyFillMode
---

# SetPolyFillMode function


## -description

The <b>SetPolyFillMode</b> function sets the polygon fill mode for functions that fill polygons.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param mode [in]

The new fill mode. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ALTERNATE"></a><a id="alternate"></a><dl>
<dt><b>ALTERNATE</b></dt>
</dl>
</td>
<td width="60%">
Selects alternate mode (fills the area between odd-numbered and even-numbered polygon sides on each scan line).

</td>
</tr>
<tr>
<td width="40%"><a id="WINDING"></a><a id="winding"></a><dl>
<dt><b>WINDING</b></dt>
</dl>
</td>
<td width="60%">
Selects winding mode (fills any region with a nonzero winding value).

</td>
</tr>
</table>

## -returns

The return value specifies the previous filling mode. If an error occurs, the return value is zero.

## -remarks

In general, the modes differ only in cases where a complex, overlapping polygon must be filled (for example, a five-sided polygon that forms a five-pointed star with a pentagon in the center). In such cases, ALTERNATE mode fills every other enclosed region within the polygon (that is, the points of the star), but WINDING mode fills all regions (that is, the points and the pentagon).

When the fill mode is ALTERNATE, GDI fills the area between odd-numbered and even-numbered polygon sides on each scan line. That is, GDI fills the area between the first and second side, between the third and fourth side, and so on.

When the fill mode is WINDING, GDI fills any region that has a nonzero winding value. This value is defined as the number of times a pen used to draw the polygon would go around the region. The direction of each edge of the polygon is important.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-getpolyfillmode">GetPolyFillMode</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>