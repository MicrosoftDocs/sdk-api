---
UID: NF:wingdi.Polygon
title: Polygon function (wingdi.h)
description: The Polygon function draws a polygon consisting of two or more vertices connected by straight lines. The polygon is outlined by using the current pen and filled by using the current brush and polygon fill mode.
helpviewer_keywords: ["Polygon","Polygon function [Windows GDI]","_win32_Polygon","gdi.polygon","wingdi/Polygon"]
old-location: gdi\polygon.htm
tech.root: gdi
ms.assetid: 2f958b91-039a-4e02-b727-be142bb18b06
ms.date: 12/05/2018
ms.keywords: Polygon, Polygon function [Windows GDI], _win32_Polygon, gdi.polygon, wingdi/Polygon
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
 - Polygon
 - wingdi/Polygon
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
 - Polygon
---

# Polygon function


## -description

The <b>Polygon</b> function draws a polygon consisting of two or more vertices connected by straight lines. The polygon is outlined by using the current pen and filled by using the current brush and polygon fill mode.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param apt [in]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that specify the vertices of the polygon, in logical coordinates.

### -param cpt [in]

The number of vertices in the array. This value must be greater than or equal to 2.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The polygon is closed automatically by drawing a line from the last vertex to the first.

The current position is neither used nor updated by the <b>Polygon</b> function.

Any extra points are ignored. To draw a line with more points, divide your data into groups, each of which have less than the maximum number of points, and call the function for each group of points. Remember to connect the line segments.

## -see-also

<a href="/windows/desktop/gdi/filled-shape-functions">Filled Shape Functions</a>



<a href="/windows/desktop/gdi/filled-shapes">Filled Shapes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getpolyfillmode">GetPolyFillMode
      </a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polypolygon">PolyPolygon
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polyline">Polyline
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polylineto">PolylineTo
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setpolyfillmode">SetPolyFillMode
      </a>