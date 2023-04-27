---
UID: NF:wingdi.PolyPolygon
title: PolyPolygon function (wingdi.h)
description: The PolyPolygon function draws a series of closed polygons. Each polygon is outlined by using the current pen and filled by using the current brush and polygon fill mode. The polygons drawn by this function can overlap.
helpviewer_keywords: ["PolyPolygon","PolyPolygon function [Windows GDI]","_win32_PolyPolygon","gdi.polypolygon","wingdi/PolyPolygon"]
old-location: gdi\polypolygon.htm
tech.root: gdi
ms.assetid: ac0a2802-c8b0-4cd7-9521-5b179f2c70b9
ms.date: 12/05/2018
ms.keywords: PolyPolygon, PolyPolygon function [Windows GDI], _win32_PolyPolygon, gdi.polypolygon, wingdi/PolyPolygon
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
 - PolyPolygon
 - wingdi/PolyPolygon
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
 - PolyPolygon
---

# PolyPolygon function


## -description

The <b>PolyPolygon</b> function draws a series of closed polygons. Each polygon is outlined by using the current pen and filled by using the current brush and polygon fill mode. The polygons drawn by this function can overlap.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param apt [in]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that define the vertices of the polygons, in logical coordinates. The polygons are specified consecutively. Each polygon is closed automatically by drawing a line from the last vertex to the first. Each vertex should be specified once.

### -param asz [in]

A pointer to an array of integers, each of which specifies the number of points in the corresponding polygon. Each integer must be greater than or equal to 2.

### -param csz [in]

The total number of polygons.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The current position is neither used nor updated by this function.

Any extra points are ignored. To draw the polygons with more points, divide your data into groups, each of which have less than the maximum number of points, and call the function for each group of points. Note, it is best to have a polygon in only one of the groups.

## -see-also

<a href="/windows/desktop/gdi/filled-shape-functions">Filled Shape Functions</a>



<a href="/windows/desktop/gdi/filled-shapes">Filled Shapes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getpolyfillmode">GetPolyFillMode
      </a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polygon">Polygon</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polyline">Polyline
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polylineto">PolylineTo
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpolyfillmode">SetPolyFillMode
      </a>