---
UID: NF:wingdi.CreateRectRgn
title: CreateRectRgn function (wingdi.h)
description: The CreateRectRgn function creates a rectangular region.
helpviewer_keywords: ["CreateRectRgn","CreateRectRgn function [Windows GDI]","_win32_CreateRectRgn","gdi.createrectrgn","wingdi/CreateRectRgn"]
old-location: gdi\createrectrgn.htm
tech.root: gdi
ms.assetid: 17456440-c655-48ab-8d1e-ee770330f164
ms.date: 12/05/2018
ms.keywords: CreateRectRgn, CreateRectRgn function [Windows GDI], _win32_CreateRectRgn, gdi.createrectrgn, wingdi/CreateRectRgn
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
 - CreateRectRgn
 - wingdi/CreateRectRgn
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
 - api-ms-win-gdi-ie-rgn-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
 - GDI32Full.dll
api_name:
 - CreateRectRgn
---

# CreateRectRgn function


## -description

The <b>CreateRectRgn</b> function creates a rectangular region.

## -parameters

### -param x1 [in]

Specifies the x-coordinate of the upper-left corner of the region in logical units.

### -param y1 [in]

Specifies the y-coordinate of the upper-left corner of the region in logical units.

### -param x2 [in]

Specifies the x-coordinate of the lower-right corner of the region in logical units.

### -param y2 [in]

Specifies the y-coordinate of the lower-right corner of the region in logical units.

## -returns

If the function succeeds, the return value is the handle to the region.

If the function fails, the return value is <b>NULL</b>.

## -remarks

When you no longer need the <b>HRGN</b> object, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

Region coordinates are represented as 27-bit signed integers.

Regions created by the Create&lt;shape&gt;Rgn methods (such as <b>CreateRectRgn</b> and <a href="/windows/desktop/api/wingdi/nf-wingdi-createpolygonrgn">CreatePolygonRgn</a>) only include the interior of the shape; the shape's outline is excluded from the region. This means that any point on a line between two sequential vertices is not included in the region. If you were to call <a href="/windows/desktop/api/wingdi/nf-wingdi-ptinregion">PtInRegion</a> for such a point, it would return zero as the result.


#### Examples

For an example, see <a href="/windows/desktop/gdi/drawing-markers">Drawing Markers.</a>


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolypolygonrgn">CreatePolyPolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolygonrgn">CreatePolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgnindirect">CreateRectRgnIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createroundrectrgn">CreateRoundRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreateregion">ExtCreateRegion</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getregiondata">GetRegionData</a>



<a href="/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="/windows/desktop/gdi/regions">Regions Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>