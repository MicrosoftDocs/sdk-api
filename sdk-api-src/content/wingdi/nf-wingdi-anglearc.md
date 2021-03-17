---
UID: NF:wingdi.AngleArc
title: AngleArc function (wingdi.h)
description: The AngleArc function draws a line segment and an arc.
helpviewer_keywords: ["AngleArc","AngleArc function [Windows GDI]","_win32_AngleArc","gdi.anglearc","wingdi/AngleArc"]
old-location: gdi\anglearc.htm
tech.root: gdi
ms.assetid: 65c38da1-ab7d-4e80-83e3-ba1db66f8fd9
ms.date: 12/05/2018
ms.keywords: AngleArc, AngleArc function [Windows GDI], _win32_AngleArc, gdi.anglearc, wingdi/AngleArc
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
 - AngleArc
 - wingdi/AngleArc
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
 - AngleArc
---

# AngleArc function


## -description

The <b>AngleArc</b> function draws a line segment and an arc. The line segment is drawn from the current position to the beginning of the arc. The arc is drawn along the perimeter of a circle with the given radius and center. The length of the arc is defined by the given start and sweep angles.

## -parameters

### -param hdc [in]

Handle to a device context.

### -param x [in]

Specifies the x-coordinate, in logical units, of the center of the circle.

### -param y [in]

Specifies the y-coordinate, in logical units, of the center of the circle.

### -param r [in]

Specifies the radius, in logical units, of the circle. This value must be positive.

### -param StartAngle [in]

Specifies the start angle, in degrees, relative to the x-axis.

### -param SweepAngle [in]

Specifies the sweep angle, in degrees, relative to the starting angle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>AngleArc</b> function moves the current position to the ending point of the arc.

The arc drawn by this function may appear to be elliptical, depending on the current transformation and mapping mode. Before drawing the arc, <b>AngleArc</b> draws the line segment from the current position to the beginning of the arc.

The arc is drawn by constructing an imaginary circle around the specified center point with the specified radius. The starting point of the arc is determined by measuring counterclockwise from the x-axis of the circle by the number of degrees in the start angle. The ending point is similarly located by measuring counterclockwise from the starting point by the number of degrees in the sweep angle.

If the sweep angle is greater than 360 degrees, the arc is swept multiple times.

This function draws lines by using the current pen. The figure is not filled.


#### Examples

For an example, see <a href="/windows/desktop/gdi/drawing-a-pie-chart">Drawing a Pie Chart</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-arc">Arc</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-arcto">ArcTo</a>



<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a>