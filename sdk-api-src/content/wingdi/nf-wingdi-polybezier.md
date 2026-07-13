---
UID: NF:wingdi.PolyBezier
title: PolyBezier function (wingdi.h)
description: The PolyBezier function draws one or more Bézier curves.
helpviewer_keywords: ["PolyBezier","PolyBezier function [Windows GDI]","_win32_PolyBezier","gdi.polybezier","wingdi/PolyBezier"]
old-location: gdi\polybezier.htm
tech.root: gdi
ms.assetid: d1622574-c65e-4265-9a17-22bb4d2cae0e
ms.date: 12/05/2018
ms.keywords: PolyBezier, PolyBezier function [Windows GDI], _win32_PolyBezier, gdi.polybezier, wingdi/PolyBezier
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
 - PolyBezier
 - wingdi/PolyBezier
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
 - PolyBezier
---

# PolyBezier function


## -description

The <b>PolyBezier</b> function draws one or more Bézier curves.

## -parameters

### -param hdc [in]

A handle to a device context.

### -param apt [in]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that contain the endpoints and control points of the curve(s), in logical units.

### -param cpt [in]

The number of points in the <i>lppt</i> array. This value must be one more than three times the number of curves to be drawn, because each Bézier curve requires two control points and an endpoint, and the initial curve requires an additional starting point.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The <b>PolyBezier</b> function draws cubic Bézier curves by using the endpoints and control points specified by the <i>lppt</i> parameter. The first curve is drawn from the first point to the fourth point by using the second and third points as control points. Each subsequent curve in the sequence needs exactly three more points: the ending point of the previous curve is used as the starting point, the next two points in the sequence are control points, and the third is the ending point.

The current position is neither used nor updated by the <b>PolyBezier</b> function. The figure is not filled.

This function draws lines by using the current pen.


#### Examples

For an example, see <a href="/windows/desktop/gdi/redrawing-in-the-update-region">Redrawing in the Update Region</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polybezierto">PolyBezierTo</a>