---
UID: NE:d2d1_1.D2D1_STROKE_TRANSFORM_TYPE
title: D2D1_STROKE_TRANSFORM_TYPE (d2d1_1.h)
description: Defines how the world transform, dots per inch (dpi), and stroke width affect the shape of the pen used to stroke a primitive.
helpviewer_keywords: ["D2D1_STROKE_TRANSFORM_TYPE","D2D1_STROKE_TRANSFORM_TYPE enumeration [Direct2D]","D2D1_STROKE_TRANSFORM_TYPE_FIXED","D2D1_STROKE_TRANSFORM_TYPE_HAIRLINE","D2D1_STROKE_TRANSFORM_TYPE_NORMAL","d2d1_1/D2D1_STROKE_TRANSFORM_TYPE","d2d1_1/D2D1_STROKE_TRANSFORM_TYPE_FIXED","d2d1_1/D2D1_STROKE_TRANSFORM_TYPE_HAIRLINE","d2d1_1/D2D1_STROKE_TRANSFORM_TYPE_NORMAL","direct2d.__d2d1_stroke_transform_type"]
old-location: direct2d\__d2d1_stroke_transform_type.htm
tech.root: Direct2D
ms.assetid: 99c2c5c8-49ce-4865-befa-e9f92905a260
ms.date: 12/05/2018
ms.keywords: D2D1_STROKE_TRANSFORM_TYPE, D2D1_STROKE_TRANSFORM_TYPE enumeration [Direct2D], D2D1_STROKE_TRANSFORM_TYPE_FIXED, D2D1_STROKE_TRANSFORM_TYPE_HAIRLINE, D2D1_STROKE_TRANSFORM_TYPE_NORMAL, d2d1_1/D2D1_STROKE_TRANSFORM_TYPE, d2d1_1/D2D1_STROKE_TRANSFORM_TYPE_FIXED, d2d1_1/D2D1_STROKE_TRANSFORM_TYPE_HAIRLINE, d2d1_1/D2D1_STROKE_TRANSFORM_TYPE_NORMAL, direct2d.__d2d1_stroke_transform_type
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: D2D1_STROKE_TRANSFORM_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_STROKE_TRANSFORM_TYPE
 - d2d1_1/D2D1_STROKE_TRANSFORM_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D2d1_1.h
api_name:
 - D2D1_STROKE_TRANSFORM_TYPE
---

# D2D1_STROKE_TRANSFORM_TYPE enumeration


## -description

Defines how the world transform, dots per inch (dpi), and stroke width affect the shape of the pen used to stroke a primitive.

## -enum-fields

### -field D2D1_STROKE_TRANSFORM_TYPE_NORMAL:0

The stroke respects the currently set world transform, the dpi, and the stroke width.

### -field D2D1_STROKE_TRANSFORM_TYPE_FIXED:1

The stroke does not respect the world transform but it does respect the dpi and stroke width.

### -field D2D1_STROKE_TRANSFORM_TYPE_HAIRLINE:2

The stroke is forced to 1 pixel wide (in device space) and does not respect the world transform, the dpi, or the stroke width.

### -field D2D1_STROKE_TRANSFORM_TYPE_FORCE_DWORD:0xffffffff

## -remarks

If you specify <b>D2D1_STROKE_TRANSFORM_TYPE_FIXED</b> the stroke isn't affected by the world transform.

If you specify <b>D2D1_STROKE_TRANSFORM_TYPE_FIXED</b> the application has the same behavior in Windows 7 and later.

If you specify <b>D2D1_STROKE_TRANSFORM_TYPE_HAIRLINE</b> the stroke is always 1 pixel wide.

Apart from the stroke, any value derived from the stroke width is not affected when the transformType is either fixed or hairline. This includes miters, line caps and so on.

 

It is important to distinguish between the geometry being stroked and the shape of the stroke pen. When D2D1_STROKE_TRANSFORM_TYPE_FIXED or D2D1_STROKE_TRANSFORM_TYPE_HAIRLINE is specified, the geometry still respects the transform and dpi, but the pen that traces the geometry will not.

Here is an illustration of a stroke with dashing and a skew and stretch transform.

<img alt="An illustration of a stroke with dashing and a skew and stretch transform." src="./images/skewedstroke.png"/>
And here is an illustration of a fixed width stroke which does not get transformed.

<img alt="An illustration of a fixed width stroke which does not get transformed." src="./images/fixedwidthstroke.png"/>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1">ID2D1StrokeStyle1</a>
