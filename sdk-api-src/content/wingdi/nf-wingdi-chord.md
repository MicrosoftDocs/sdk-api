---
UID: NF:wingdi.Chord
title: Chord function (wingdi.h)
description: The Chord function draws a chord (a region bounded by the intersection of an ellipse and a line segment, called a secant). The chord is outlined by using the current pen and filled by using the current brush.
helpviewer_keywords: ["Chord","Chord function [Windows GDI]","_win32_Chord","gdi.chord","wingdi/Chord"]
old-location: gdi\chord.htm
tech.root: gdi
ms.assetid: d6752c47-96a5-4fac-a1bb-0611a91f03f9
ms.date: 12/05/2018
ms.keywords: Chord, Chord function [Windows GDI], _win32_Chord, gdi.chord, wingdi/Chord
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
 - Chord
 - wingdi/Chord
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
 - Chord
---

# Chord function


## -description

The <b>Chord</b> function draws a chord (a region bounded by the intersection of an ellipse and a line segment, called a secant). The chord is outlined by using the current pen and filled by using the current brush.

## -parameters

### -param hdc [in]

A handle to the device context in which the chord appears.

### -param x1 [in]

The x-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.

### -param y1 [in]

The y-coordinate, in logical coordinates, of the upper-left corner of the bounding rectangle.

### -param x2 [in]

The x-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.

### -param y2 [in]

The y-coordinate, in logical coordinates, of the lower-right corner of the bounding rectangle.

### -param x3 [in]

The x-coordinate, in logical coordinates, of the endpoint of the radial defining the beginning of the chord.

### -param y3 [in]

The y-coordinate, in logical coordinates, of the endpoint of the radial defining the beginning of the chord.

### -param x4 [in]

The x-coordinate, in logical coordinates, of the endpoint of the radial defining the end of the chord.

### -param y4 [in]

The y-coordinate, in logical coordinates, of the endpoint of the radial defining the end of the chord.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The curve of the chord is defined by an ellipse that fits the specified bounding rectangle. The curve begins at the point where the ellipse intersects the first radial and extends counterclockwise to the point where the ellipse intersects the second radial. The chord is closed by drawing a line from the intersection of the first radial and the curve to the intersection of the second radial and the curve.

If the starting point and ending point of the curve are the same, a complete ellipse is drawn.

The current position is neither used nor updated by <b>Chord</b>.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-anglearc">AngleArc
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-arc">Arc
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-arcto">ArcTo
      </a>



<a href="/windows/desktop/gdi/filled-shape-functions">Filled Shape Functions</a>



<a href="/windows/desktop/gdi/filled-shapes">Filled Shapes Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-pie">Pie
      </a>