---
UID: NF:wingdi.PolyBezierTo
title: PolyBezierTo function (wingdi.h)
description: The PolyBezierTo function draws one or more Bézier curves.
helpviewer_keywords: ["PolyBezierTo","PolyBezierTo function [Windows GDI]","_win32_PolyBezierTo","gdi.polybezierto","wingdi/PolyBezierTo"]
old-location: gdi\polybezierto.htm
tech.root: gdi
ms.assetid: 0c8d6d6d-d0a3-4188-91ad-934e6f054862
ms.date: 12/05/2018
ms.keywords: PolyBezierTo, PolyBezierTo function [Windows GDI], _win32_PolyBezierTo, gdi.polybezierto, wingdi/PolyBezierTo
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
 - PolyBezierTo
 - wingdi/PolyBezierTo
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
 - PolyBezierTo
---

# PolyBezierTo function


## -description

The <b>PolyBezierTo</b> function draws one or more Bézier curves.

## -parameters

### -param hdc [in]

A handle to a device context.

### -param apt [in]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that contains the endpoints and control points, in logical units.

### -param cpt [in]

The number of points in the <i>lppt</i> array. This value must be three times the number of curves to be drawn because each Bézier curve requires two control points and an ending point.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

This function draws cubic Bézier curves by using the control points specified by the <i>lppt</i> parameter. The first curve is drawn from the current position to the third point by using the first two points as control points. For each subsequent curve, the function needs exactly three more points, and uses the ending point of the previous curve as the starting point for the next.

<b>PolyBezierTo</b> moves the current position to the ending point of the last Bézier curve. The figure is not filled.

This function draws lines by using the current pen.

## -see-also

<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polybezier">PolyBezier</a>