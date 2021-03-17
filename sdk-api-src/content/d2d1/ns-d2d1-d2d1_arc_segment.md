---
UID: NS:d2d1.D2D1_ARC_SEGMENT
title: D2D1_ARC_SEGMENT (d2d1.h)
description: Describes an elliptical arc between two points.
helpviewer_keywords: ["D2D1_ARC_SEGMENT","D2D1_ARC_SEGMENT structure [Direct2D]","d2d1/D2D1_ARC_SEGMENT","direct2d.D2D1_ARC_SEGMENT"]
old-location: direct2d\D2D1_ARC_SEGMENT.htm
tech.root: Direct2D
ms.assetid: 3f391265-20b4-4897-aa0b-d14b71cd5f0a
ms.date: 12/05/2018
ms.keywords: D2D1_ARC_SEGMENT, D2D1_ARC_SEGMENT structure [Direct2D], d2d1/D2D1_ARC_SEGMENT, direct2d.D2D1_ARC_SEGMENT
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
req.typenames: D2D1_ARC_SEGMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_ARC_SEGMENT
 - d2d1/D2D1_ARC_SEGMENT
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
 - D2D1_ARC_SEGMENT
---

# D2D1_ARC_SEGMENT structure


## -description

Describes an elliptical arc between two points.

## -struct-fields

### -field point

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

The end point of the arc.

### -field size

Type: <b><a href="/windows/win32/Direct2D/d2d1-size-f">D2D1_SIZE_F</a></b>

The x-radius and y-radius of the arc.

### -field rotationAngle

Type: <b>FLOAT</b>

A value that specifies how many degrees in the clockwise direction the ellipse is rotated relative to the current coordinate system.

### -field sweepDirection

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_sweep_direction">D2D1_SWEEP_DIRECTION</a></b>

A value that specifies whether the arc sweep is clockwise or counterclockwise.

### -field arcSize

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_arc_size">D2D1_ARC_SIZE</a></b>

A value that specifies whether the given arc is larger than 180 degrees.

