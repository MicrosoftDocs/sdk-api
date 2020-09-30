---
UID: NF:d2d1helper.BezierSegment
title: BezierSegment function (d2d1helper.h)
description: Creates a D2D1_BEZIER_SEGMENT structure.
helpviewer_keywords: ["BezierSegment","BezierSegment function [Direct2D]","d2d1helper/BezierSegment","direct2d.beziersegment"]
old-location: direct2d\beziersegment.htm
tech.root: Direct2D
ms.assetid: 50938354-f9b7-40a9-807d-708f6a065912
ms.date: 12/05/2018
ms.keywords: BezierSegment, BezierSegment function [Direct2D], d2d1helper/BezierSegment, direct2d.beziersegment
req.header: d2d1helper.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BezierSegment
 - d2d1helper/BezierSegment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - BezierSegment
---

# BezierSegment function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment">D2D1_BEZIER_SEGMENT</a> structure.

## -parameters

### -param point1 [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The first control point for the Bezier segment.

### -param point2 [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The second control point for the Bezier segment.

### -param point3 [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The end point for the Bezier segment.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment">D2D1_BEZIER_SEGMENT</a></b>

The new Bezier segment.

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1geometrysink">ID2D1GeometrySink</a>