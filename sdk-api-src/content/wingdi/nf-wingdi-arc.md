---
UID: NF:wingdi.Arc
title: Arc function (wingdi.h)
description: The Arc function draws an elliptical arc.
helpviewer_keywords: ["Arc","Arc function [Windows GDI]","_win32_Arc","gdi.arc","wingdi/Arc"]
old-location: gdi\arc.htm
tech.root: gdi
ms.assetid: c15a2173-0fad-4a8a-b0f9-cd39fe4e7bac
ms.date: 12/05/2018
ms.keywords: Arc, Arc function [Windows GDI], _win32_Arc, gdi.arc, wingdi/Arc
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
 - Arc
 - wingdi/Arc
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
 - Arc
---

# Arc function


## -description

The <b>Arc</b> function draws an elliptical arc.

## -parameters

### -param hdc [in]

A handle to the device context where drawing takes place.

### -param x1 [in]

The x-coordinate, in logical units, of the upper-left corner of the bounding rectangle.

### -param y1 [in]

The y-coordinate, in logical units, of the upper-left corner of the bounding rectangle.

### -param x2 [in]

The x-coordinate, in logical units, of the lower-right corner of the bounding rectangle.

### -param y2 [in]

The y-coordinate, in logical units, of the lower-right corner of the bounding rectangle.

### -param x3 [in]

The x-coordinate, in logical units, of the ending point of the radial line defining the starting point of the arc.

### -param y3 [in]

The y-coordinate, in logical units, of the ending point of the radial line defining the starting point of the arc.

### -param x4 [in]

The x-coordinate, in logical units, of the ending point of the radial line defining the ending point of the arc.

### -param y4 [in]

The y-coordinate, in logical units, of the ending point of the radial line defining the ending point of the arc.

## -returns

If the arc is drawn, the return value is nonzero.

If the arc is not drawn, the return value is zero.

## -remarks

The points (<i>nLeftRect</i>, <i>nTopRect</i>) and (<i>nRightRect</i>, <i>nBottomRect</i>) specify the bounding rectangle. An ellipse formed by the specified bounding rectangle defines the curve of the arc. The arc extends in the current drawing direction from the point where it intersects the radial from the center of the bounding rectangle to the (<i>nXStartArc</i>, <i>nYStartArc</i>) point. The arc ends where it intersects the radial from the center of the bounding rectangle to the (<i>nXEndArc</i>, <i>nYEndArc</i>) point. If the starting point and ending point are the same, a complete ellipse is drawn.

The arc is drawn using the current pen; it is not filled.

The current position is neither used nor updated by <b>Arc</b>.

Use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getarcdirection">GetArcDirection</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-setarcdirection">SetArcDirection</a> functions to get and set the current drawing direction for a device context. The default drawing direction is counterclockwise.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-anglearc">AngleArc</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-arcto">ArcTo</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-chord">Chord</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-ellipse">Ellipse</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getarcdirection">GetArcDirection</a>



<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-pie">Pie</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setarcdirection">SetArcDirection</a>