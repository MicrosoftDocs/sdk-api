---
UID: NF:wingdi.ArcTo
title: ArcTo function (wingdi.h)
description: The ArcTo function draws an elliptical arc.
helpviewer_keywords: ["ArcTo","ArcTo function [Windows GDI]","_win32_ArcTo","gdi.arcto","wingdi/ArcTo"]
old-location: gdi\arcto.htm
tech.root: gdi
ms.assetid: 5e358a14-9f39-4267-9a44-c8bf05b5dfbb
ms.date: 12/05/2018
ms.keywords: ArcTo, ArcTo function [Windows GDI], _win32_ArcTo, gdi.arcto, wingdi/ArcTo
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
 - ArcTo
 - wingdi/ArcTo
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
 - ArcTo
---

# ArcTo function


## -description

The <b>ArcTo</b> function draws an elliptical arc.

## -parameters

### -param hdc [in]

A handle to the device context where drawing takes place.

### -param left [in]

The x-coordinate, in logical units, of the upper-left corner of the bounding rectangle.

### -param top [in]

The y-coordinate, in logical units, of the upper-left corner of the bounding rectangle.

### -param right [in]

The x-coordinate, in logical units, of the lower-right corner of the bounding rectangle.

### -param bottom [in]

The y-coordinate, in logical units, of the lower-right corner of the bounding rectangle.

### -param xr1 [in]

The x-coordinate, in logical units, of the endpoint of the radial defining the starting point of the arc.

### -param yr1 [in]

The y-coordinate, in logical units, of the endpoint of the radial defining the starting point of the arc.

### -param xr2 [in]

The x-coordinate, in logical units, of the endpoint of the radial defining the ending point of the arc.

### -param yr2 [in]

The y-coordinate, in logical units, of the endpoint of the radial defining the ending point of the arc.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

<b>ArcTo</b> is similar to the <a href="/windows/desktop/api/wingdi/nf-wingdi-arc">Arc</a> function, except that the current position is updated.

The points (<i>nLeftRect</i>, <i>nTopRect</i>) and (<i>nRightRect</i>, <i>nBottomRect</i>) specify the bounding rectangle. An ellipse formed by the specified bounding rectangle defines the curve of the arc. The arc extends counterclockwise from the point where it intersects the radial line from the center of the bounding rectangle to the (<i>nXRadial1</i>, <i>nYRadial1</i>) point. The arc ends where it intersects the radial line from the center of the bounding rectangle to the (<i>nXRadial2</i>, <i>nYRadial2</i>) point. If the starting point and ending point are the same, a complete ellipse is drawn.

A line is drawn from the current position to the starting point of the arc. If no error occurs, the current position is set to the ending point of the arc.

The arc is drawn using the current pen; it is not filled.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-anglearc">AngleArc</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-arc">Arc</a>



<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setarcdirection">SetArcDirection</a>