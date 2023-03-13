---
UID: NF:wingdi.PolyPolyline
title: PolyPolyline function (wingdi.h)
description: The PolyPolyline function draws multiple series of connected line segments.
helpviewer_keywords: ["PolyPolyline","PolyPolyline function [Windows GDI]","_win32_PolyPolyline","gdi.polypolyline","wingdi/PolyPolyline"]
old-location: gdi\polypolyline.htm
tech.root: gdi
ms.assetid: 71a9273f-321b-4efb-ac73-5979f8151d05
ms.date: 12/05/2018
ms.keywords: PolyPolyline, PolyPolyline function [Windows GDI], _win32_PolyPolyline, gdi.polypolyline, wingdi/PolyPolyline
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
 - PolyPolyline
 - wingdi/PolyPolyline
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
 - PolyPolyline
---

# PolyPolyline function


## -description

The <b>PolyPolyline</b> function draws multiple series of connected line segments.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param apt [in]

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that contains the vertices of the polylines, in logical units. The polylines are specified consecutively.

### -param asz [in]

A pointer to an array of variables specifying the number of points in the <i>lppt</i> array for the corresponding polyline. Each entry must be greater than or equal to two.

### -param csz [in]

The total number of entries in the <i>lpdwPolyPoints</i> array.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The line segments are drawn by using the current pen. The figures formed by the segments are not filled.

The current position is neither used nor updated by this function.

## -see-also

<a href="/windows/desktop/gdi/line-and-curve-functions">Line and Curve Functions</a>



<a href="/windows/desktop/gdi/lines-and-curves">Lines and Curves Overview</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polyline">Polyline</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-polylineto">PolylineTo</a>