---
UID: NF:wingdi.LineTo
title: LineTo function (wingdi.h)
description: The LineTo function draws a line from the current position up to, but not including, the specified point.
helpviewer_keywords: ["LineTo","LineTo function [Windows GDI]","_win32_LineTo","gdi.lineto","wingdi/LineTo"]
old-location: gdi\lineto.htm
tech.root: gdi
ms.assetid: a31b3a9a-110f-4cdf-89d9-19937a2e40b4
ms.date: 12/05/2018
ms.keywords: LineTo, LineTo function [Windows GDI], _win32_LineTo, gdi.lineto, wingdi/LineTo
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
 - LineTo
 - wingdi/LineTo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - LineTo
---

# LineTo function


## -description

The <b>LineTo</b> function draws a line from the current position up to, but not including, the specified point.

## -parameters

### -param hdc [in]

Handle to a device context.

### -param x [in]

Specifies the x-coordinate, in logical units, of the line's ending point.

### -param y [in]

Specifies the y-coordinate, in logical units, of the line's ending point.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The line is drawn by using the current pen and, if the pen is a geometric pen, the current brush.

If <b>LineTo</b> succeeds, the current position is set to the specified ending point.


#### Examples

For an example, see <a href="/windows/desktop/gdi/drawing-markers">Drawing Markers</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polyline">Polyline</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polylineto">PolylineTo</a>