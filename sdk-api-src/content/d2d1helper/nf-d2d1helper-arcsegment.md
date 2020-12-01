---
UID: NF:d2d1helper.ArcSegment
title: ArcSegment function (d2d1helper.h)
description: Creates a D2D1_ARC_SEGMENT structure.
helpviewer_keywords: ["ArcSegment","ArcSegment function [Direct2D]","d2d1helper/ArcSegment","direct2d.arcsegment"]
old-location: direct2d\arcsegment.htm
tech.root: Direct2D
ms.assetid: 0a2e7b92-2d0a-4898-ad3e-2142347e8c31
ms.date: 12/05/2018
ms.keywords: ArcSegment, ArcSegment function [Direct2D], d2d1helper/ArcSegment, direct2d.arcsegment
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
 - ArcSegment
 - d2d1helper/ArcSegment
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
 - ArcSegment
---

# ArcSegment function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_arc_segment">D2D1_ARC_SEGMENT</a> structure.

## -parameters

### -param point [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The end point of the arc.

### -param size [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-size-f">D2D1_SIZE_F</a></b>

The x-radius and y-radius of the arc.

### -param rotationAngle [in]

Type: <b>FLOAT</b>

The number of degrees that the ellipse is rotated relative to the current coordinate system. A positive number specifies a clockwise rotation and a negative number specifies a counterclockwise rotation.

### -param sweepDirection [in]

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_sweep_direction">D2D1_SWEEP_DIRECTION</a></b>

A value that specifies whether the arc sweep is clockwise or counterclockwise.

### -param arcSize [in]

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_arc_size">D2D1_ARC_SIZE</a></b>

A value  that specifies whether the arc is larger than 180 degrees.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_arc_segment">D2D1_ARC_SEGMENT</a></b>

The new arc segment.

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1geometrysink">ID2D1GeometrySink</a>