---
UID: NF:wingdi.PolylineTo
title: PolylineTo function (wingdi.h)
description: The PolylineTo function draws one or more straight lines.
helpviewer_keywords: ["PolylineTo","PolylineTo function [Windows GDI]","_win32_PolylineTo","gdi.polylineto","wingdi/PolylineTo"]
old-location: gdi\polylineto.htm
tech.root: gdi
ms.assetid: 76020742-b651-4244-82c3-13034573c306
ms.date: 12/05/2018
ms.keywords: PolylineTo, PolylineTo function [Windows GDI], _win32_PolylineTo, gdi.polylineto, wingdi/PolylineTo
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
 - PolylineTo
 - wingdi/PolylineTo
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
api_name:
 - PolylineTo
---

# PolylineTo function


## -description

The <b>PolylineTo</b> function draws one or more straight lines.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param apt [in]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that contains the vertices of the line, in logical units.

### -param cpt [in]

The number of points in the array.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Unlike the <a href="/windows/desktop/api/wingdi/nf-wingdi-polyline">Polyline</a> function, the <b>PolylineTo</b> function uses and updates the current position.

A line is drawn from the current position to the first point specified by the <i>lppt</i> parameter by using the current pen. For each additional line, the function draws from the ending point of the previous line to the next point specified by <i>lppt</i>.

<b>PolylineTo</b> moves the current position to the ending point of the last line.

If the line segments drawn by this function form a closed figure, the figure is not filled.

## -see-also

<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polypolyline">PolyPolyline</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polyline">Polyline</a>