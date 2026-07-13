---
UID: NF:wingdi.CreatePolygonRgn
title: CreatePolygonRgn function (wingdi.h)
description: The CreatePolygonRgn function creates a polygonal region.
helpviewer_keywords: ["ALTERNATE","CreatePolygonRgn","CreatePolygonRgn function [Windows GDI]","WINDING","_win32_CreatePolygonRgn","gdi.createpolygonrgn","wingdi/CreatePolygonRgn"]
old-location: gdi\createpolygonrgn.htm
tech.root: gdi
ms.assetid: dd7ad6de-c5f2-46e4-8d28-24caaa48ba3a
ms.date: 12/05/2018
ms.keywords: ALTERNATE, CreatePolygonRgn, CreatePolygonRgn function [Windows GDI], WINDING, _win32_CreatePolygonRgn, gdi.createpolygonrgn, wingdi/CreatePolygonRgn
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
 - CreatePolygonRgn
 - wingdi/CreatePolygonRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
api_name:
 - CreatePolygonRgn
---

# CreatePolygonRgn function


## -description

The <b>CreatePolygonRgn</b> function creates a polygonal region.

## -parameters

### -param pptl [in]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that define the vertices of the polygon in logical units. The polygon is presumed closed. Each vertex can be specified only once.

### -param cPoint [in]

The number of points in the array.

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

If the function fails, the return value is <b>NULL</b>.

## -remarks

When you no longer need the <b>HRGN</b> object, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

Region coordinates are represented as 27-bit signed integers.

Regions created by the Create&lt;shape&gt;Rgn methods (such as <a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a> and <b>CreatePolygonRgn</b>) only include the interior of the shape; the shape's outline is excluded from the region. This means that any point on a line between two sequential vertices is not included in the region. If you were to call <a href="/windows/desktop/api/wingdi/nf-wingdi-ptinregion">PtInRegion</a> for such a point, it would return zero as the result.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolypolygonrgn">CreatePolyPolygonRgn</a>



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