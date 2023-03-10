---
UID: NF:wingdi.Polyline
title: Polyline function (wingdi.h)
description: The Polyline function draws a series of line segments by connecting the points in the specified array.
helpviewer_keywords: ["Polyline","Polyline function [Windows GDI]","_win32_Polyline","gdi.polyline","wingdi/Polyline"]
old-location: gdi\polyline.htm
tech.root: gdi
ms.assetid: 55481dd0-3db7-4131-b383-4d0036943e60
ms.date: 12/05/2018
ms.keywords: Polyline, Polyline function [Windows GDI], _win32_Polyline, gdi.polyline, wingdi/Polyline
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
 - Polyline
 - wingdi/Polyline
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - Polyline
---

# Polyline function


## -description

The <b>Polyline</b> function draws a series of line segments by connecting the points in the specified array.

## -parameters

### -param hdc [in]

A handle to a device context.

### -param apt [in]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures, in logical units.

### -param cpt [in]

The number of points in the array. This number must be greater than or equal to two.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The lines are drawn from the first point through subsequent points by using the current pen. Unlike the <a href="/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a> or <a href="/windows/desktop/api/wingdi/nf-wingdi-polylineto">PolylineTo</a> functions, the <b>Polyline</b> function neither uses nor updates the current position.

## -see-also

<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-lineto">LineTo</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-movetoex">MoveToEx</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polypolyline">PolyPolyline</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polylineto">PolylineTo</a>