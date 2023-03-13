---
UID: NS:d2d1_1.D2D1_STROKE_STYLE_PROPERTIES1
title: D2D1_STROKE_STYLE_PROPERTIES1 (d2d1_1.h)
description: Describes the stroke that outlines a shape. (D2D1_STROKE_STYLE_PROPERTIES1)
helpviewer_keywords: ["D2D1_STROKE_STYLE_PROPERTIES1","D2D1_STROKE_STYLE_PROPERTIES1 structure [Direct2D]","PD2D1_STROKE_STYLE_PROPERTIES1","PD2D1_STROKE_STYLE_PROPERTIES1 structure pointer [Direct2D]","d2d1_1/D2D1_STROKE_STYLE_PROPERTIES1","d2d1_1/PD2D1_STROKE_STYLE_PROPERTIES1","direct2d.d2d1_stroke_style_properties1"]
old-location: direct2d\d2d1_stroke_style_properties1.htm
tech.root: Direct2D
ms.assetid: 6bed0f23-be10-4265-8edd-ccf82ce0e683
ms.date: 12/05/2018
ms.keywords: D2D1_STROKE_STYLE_PROPERTIES1, D2D1_STROKE_STYLE_PROPERTIES1 structure [Direct2D], PD2D1_STROKE_STYLE_PROPERTIES1, PD2D1_STROKE_STYLE_PROPERTIES1 structure pointer [Direct2D], d2d1_1/D2D1_STROKE_STYLE_PROPERTIES1, d2d1_1/PD2D1_STROKE_STYLE_PROPERTIES1, direct2d.d2d1_stroke_style_properties1
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
req.type-library: D2D1.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_STROKE_STYLE_PROPERTIES1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_STROKE_STYLE_PROPERTIES1
 - d2d1_1/D2D1_STROKE_STYLE_PROPERTIES1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_STROKE_STYLE_PROPERTIES1
---

# D2D1_STROKE_STYLE_PROPERTIES1 structure


## -description

Describes the stroke that outlines a shape.

## -struct-fields

### -field startCap

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE</a></b>

The cap to use at the start of each open figure.

### -field endCap

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE</a></b>

The cap to use at the end of each open figure.

### -field dashCap

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_cap_style">D2D1_CAP_STYLE</a></b>

The cap to use at the start and end of each dash.

### -field lineJoin

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_line_join">D2D1_LINE_JOIN</a></b>

The line join to use.

### -field miterLimit

Type: <b>FLOAT</b>

The limit beyond which miters are either clamped or converted to bevels.

### -field dashStyle

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style">D2D1_DASH_STYLE</a></b>

The type of dash to use.

### -field dashOffset

Type: <b>FLOAT</b>

The location of the first dash, relative to the start of the figure.

### -field transformType

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_stroke_transform_type">D2D1_STROKE_TRANSFORM_TYPE</a></b>

The rule that determines what render target properties affect the nib of the stroke.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-createstrokestyle(constd2d1_stroke_style_properties1_constfloat_uint32_id2d1strokestyle1)">ID2D1Factory1::CreateStrokeStyle</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1">ID2D1StrokeStyle1</a>
