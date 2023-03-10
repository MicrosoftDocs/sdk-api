---
UID: NF:wingdi.CreatePolyPolygonRgn
title: CreatePolyPolygonRgn function (wingdi.h)
description: The CreatePolyPolygonRgn function creates a region consisting of a series of polygons. The polygons can overlap.
helpviewer_keywords: ["ALTERNATE","CreatePolyPolygonRgn","CreatePolyPolygonRgn function [Windows GDI]","WINDING","_win32_CreatePolyPolygonRgn","gdi.createpolypolygonrgn","wingdi/CreatePolyPolygonRgn"]
old-location: gdi\createpolypolygonrgn.htm
tech.root: gdi
ms.assetid: 1113d3dc-8e3f-436c-a5a8-191785bc7fcc
ms.date: 12/05/2018
ms.keywords: ALTERNATE, CreatePolyPolygonRgn, CreatePolyPolygonRgn function [Windows GDI], WINDING, _win32_CreatePolyPolygonRgn, gdi.createpolypolygonrgn, wingdi/CreatePolyPolygonRgn
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
 - CreatePolyPolygonRgn
 - wingdi/CreatePolyPolygonRgn
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
 - CreatePolyPolygonRgn
---

# CreatePolyPolygonRgn function


## -description

The <b>CreatePolyPolygonRgn</b> function creates a region consisting of a series of polygons. The polygons can overlap.

## -parameters

### -param pptl [in]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that define the vertices of the polygons in logical units. The polygons are specified consecutively. Each polygon is presumed closed and each vertex is specified only once.

### -param pc [in]

A pointer to an array of integers, each of which specifies the number of points in one of the polygons in the array pointed to by <i>lppt</i>.

### -param cPoly [in]

The total number of integers in the array pointed to by <i>lpPolyCounts</i>.

### -param iMode [in]

The fill mode used to determine which pixels are in the region. This parameter can be one of the following values.

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
Selects alternate mode (fills area between odd-numbered and even-numbered polygon sides on each scan line).

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
 

For more information about these modes, see the <a href="/windows/desktop/api/wingdi/nf-wingdi-setpolyfillmode">SetPolyFillMode</a> function.

## -returns

If the function succeeds, the return value is the handle to the region.

If the function fails, the return value is zero.

## -remarks

When you no longer need the <b>HRGN</b> object, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

Region coordinates are represented as 27-bit signed integers.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolygonrgn">CreatePolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgnindirect">CreateRectRgnIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createroundrectrgn">CreateRoundRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreateregion">ExtCreateRegion</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getregiondata">GetRegionData</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpolyfillmode">SetPolyFillMode</a>