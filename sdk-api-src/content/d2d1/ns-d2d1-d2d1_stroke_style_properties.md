---
UID: NS:d2d1.D2D1_STROKE_STYLE_PROPERTIES
title: D2D1_STROKE_STYLE_PROPERTIES (d2d1.h)
description: Describes the stroke that outlines a shape. (D2D1_STROKE_STYLE_PROPERTIES)
helpviewer_keywords: ["D2D1_STROKE_STYLE_PROPERTIES","D2D1_STROKE_STYLE_PROPERTIES structure [Direct2D]","d2d1/D2D1_STROKE_STYLE_PROPERTIES","direct2d.D2D1_STROKE_STYLE_PROPERTIES"]
old-location: direct2d\D2D1_STROKE_STYLE_PROPERTIES.htm
tech.root: Direct2D
ms.assetid: 67f3701f-febd-4afe-803e-c5d9dbcd1b21
ms.date: 12/05/2018
ms.keywords: D2D1_STROKE_STYLE_PROPERTIES, D2D1_STROKE_STYLE_PROPERTIES structure [Direct2D], d2d1/D2D1_STROKE_STYLE_PROPERTIES, direct2d.D2D1_STROKE_STYLE_PROPERTIES
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
req.typenames: D2D1_STROKE_STYLE_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_STROKE_STYLE_PROPERTIES
 - d2d1/D2D1_STROKE_STYLE_PROPERTIES
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
 - D2D1_STROKE_STYLE_PROPERTIES
---

# D2D1_STROKE_STYLE_PROPERTIES structure


## -description

Describes the stroke that outlines a shape.

## -struct-fields

### -field startCap

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE</a></b>

The cap applied to the start of all the open figures in a stroked geometry.

### -field endCap

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE</a></b>

The cap applied to the end of all the open figures in a stroked geometry.

### -field dashCap

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE</a></b>

The shape  at either end of each dash segment.

### -field lineJoin

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_line_join">D2D1_LINE_JOIN</a></b>

A value that describes how segments are joined. This value is ignored for a vertex if the segment flags specify that the segment should have a smooth join.

### -field miterLimit

Type: <b>FLOAT</b>

The limit of the thickness of the join on a mitered corner. This value is always treated as though it is greater than or equal to 1.0f.

### -field dashStyle

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_dash_style">D2D1_DASH_STYLE</a></b>

A value that specifies whether the stroke has a dash pattern and, if so, the dash style.

### -field dashOffset

Type: <b>FLOAT</b>

A value that specifies an offset in the dash sequence.   A positive dash offset value  shifts the dash pattern, in units of  stroke width, toward the start of the stroked geometry.  A negative dash offset value  shifts the dash pattern, in units of  stroke width, toward the end of the stroked geometry.

## -remarks

The following illustration shows different <i>dashOffset</i> values for the same custom dash style.

<img alt="Illustration of four dashes with the same style and different dashOffset values" src="./images/StrokeStyle_DashOffset.png"/>

