---
UID: NS:d2d1.D2D1_BEZIER_SEGMENT
title: D2D1_BEZIER_SEGMENT (d2d1.h)
description: Represents a cubic bezier segment drawn between two points.
helpviewer_keywords: ["D2D1_BEZIER_SEGMENT","D2D1_BEZIER_SEGMENT structure [Direct2D]","d2d1/D2D1_BEZIER_SEGMENT","direct2d.D2D1_BEZIER_SEGMENT"]
old-location: direct2d\D2D1_BEZIER_SEGMENT.htm
tech.root: Direct2D
ms.assetid: cf8df7d2-c4fe-4a46-a4b2-7e0eed67df2a
ms.date: 12/05/2018
ms.keywords: D2D1_BEZIER_SEGMENT, D2D1_BEZIER_SEGMENT structure [Direct2D], d2d1/D2D1_BEZIER_SEGMENT, direct2d.D2D1_BEZIER_SEGMENT
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_BEZIER_SEGMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BEZIER_SEGMENT
 - d2d1/D2D1_BEZIER_SEGMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_BEZIER_SEGMENT
---

# D2D1_BEZIER_SEGMENT structure


## -description

Represents a cubic bezier segment drawn  between two points.

## -struct-fields

### -field point1

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The first control point for the Bezier segment.

### -field point2

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The second control point for the Bezier segment.

### -field point3

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The end point for the Bezier segment.

## -remarks

A cubic Bezier curve is defined by four points: a start point, an end point (<i>point3</i>), and two control points (<i>point1</i> and <i>point2</i>). A Bezier segment does not contain a property for the starting point of the curve; it defines only the end point. The beginning point of the curve is the current point of the path to which the Bezier curve is added.

The two control points of a cubic Bezier curve behave like magnets, attracting portions of what would otherwise be a straight line toward themselves and producing a curve. The first control point, <i>point1</i>, affects the beginning portion of the curve; the second control point, <i>point2</i>, affects the ending portion of the curve. 

<div class="alert"><b>Note</b>  The curve doesn't necessarily pass through either of the control points; each control point moves its portion of the line toward itself, but not through itself.</div>
<div> </div>

