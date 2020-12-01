---
UID: NF:d2d1helper.RadialGradientBrushProperties
title: RadialGradientBrushProperties function (d2d1helper.h)
description: Creates a D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES structure.
helpviewer_keywords: ["RadialGradientBrushProperties","RadialGradientBrushProperties function [Direct2D]","d2d1helper/RadialGradientBrushProperties","direct2d.radialgradientbrushproperties"]
old-location: direct2d\radialgradientbrushproperties.htm
tech.root: Direct2D
ms.assetid: d65ee26c-28d4-4b58-9089-1aab959246cc
ms.date: 12/05/2018
ms.keywords: RadialGradientBrushProperties, RadialGradientBrushProperties function [Direct2D], d2d1helper/RadialGradientBrushProperties, direct2d.radialgradientbrushproperties
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
 - RadialGradientBrushProperties
 - d2d1helper/RadialGradientBrushProperties
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
 - RadialGradientBrushProperties
---

# RadialGradientBrushProperties function


## -description

Creates a <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties">D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES</a> structure.

## -parameters

### -param center [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

In the brush's coordinate space, the center of the gradient ellipse.

### -param gradientOriginOffset [in, ref]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

In the brush's coordinate space, the offset of the gradient origin relative to the gradient ellipse's center.

### -param radiusX [in]

Type: <b>const FLOAT</b>

In the brush's coordinate space, the x-radius of the gradient ellipse.

### -param radiusY [in]

Type: <b>const FLOAT</b>

In the brush's coordinate space, the y-radius of the gradient ellipse.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties">D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES</a></b>

A structure that contains the gradient origin offset and the size and position of the gradient ellipse for an <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>.