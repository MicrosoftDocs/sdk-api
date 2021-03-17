---
UID: NS:d2d1.D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES
title: D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES (d2d1.h)
description: Contains the gradient origin offset and the size and position of the gradient ellipse for an ID2D1RadialGradientBrush.
helpviewer_keywords: ["D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES","D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES structure [Direct2D]","d2d1/D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES","direct2d.D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES"]
old-location: direct2d\D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES.htm
tech.root: Direct2D
ms.assetid: 194f7624-ac3b-4054-8d6f-5b4c99ef6546
ms.date: 12/05/2018
ms.keywords: D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES, D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES structure [Direct2D], d2d1/D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES, direct2d.D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES
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
req.typenames: D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES
 - d2d1/D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES
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
 - D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES
---

# D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES structure


## -description

Contains the gradient origin offset and the size and position of the gradient ellipse for an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>.

## -struct-fields

### -field center

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

In the brush's coordinate space, the center of the gradient ellipse.

### -field gradientOriginOffset

Type: <b><a href="/windows/win32/Direct2D/d2d1-point-2f">D2D1_POINT_2F</a></b>

In the brush's coordinate space, the offset of the gradient origin relative to the gradient ellipse's center.

### -field radiusX

Type: <b>FLOAT</b>

In the brush's coordinate space, the x-radius  of the gradient ellipse.

### -field radiusY

Type: <b>FLOAT</b>

In the brush's coordinate space, the y-radius  of the gradient ellipse.

## -remarks

Different values for <i>center</i>,  <i>gradientOriginOffset</i>,  <i>radiusX</i> and/or <i>radiusY</i> produce different gradients.   The following illustration shows several radial gradients that have different gradient origin offsets, creating the appearance of the light illuminating the circles from different angles.

<img alt="Illustration of four circles with radial gradients that have different origin offsets" src="./images/RadialGradient.png"/>

For convenience, Direct2D provides the <a href="/windows/win32/api/d2d1helper/nf-d2d1helper-radialgradientbrushproperties">D2D1::RadialGradientBrushProperties</a> function for creating new <b>D2D1_RADIAL_GRADIENT_BRUSH</b> structures.


## Examples

The following example calls <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)">CreateRadialGradientBrush</a> to create an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>. It uses the <a href="/windows/win32/api/d2d1helper/nf-d2d1helper-radialgradientbrushproperties">D2D1::RadialGradientBrushProperties</a> helper function to create a <b>D2D1_RADIAL_GRADIENT_BRUSH</b> structure that has a <i>center</i> value of (75, 5), a <i>gradientOriginOffset</i> of (0, 0), and a <i>radiusX</i> and <i>radiusY</i> of to 75 and passes the structure to the <b>CreateRadialGradientBrush</b> method.   When the gradient brush is used to fill a rectangle, it produces output as shown in the following illustration.

<img alt="Illustration of a circle with a radial gradient brush" src="./images/brushes_ovw_radials.png"/>


```cpp
// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &m_pRadialGradientBrush
        );
}

```


For more information about radial gradient brushes, see the <a href="/windows/win32/Direct2D/how-to-create-a-radial-gradient-brush">How to Create a Radial Gradient Brush</a> topic and the <a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="/windows/win32/api/d2d1helper/nf-d2d1helper-radialgradientbrushproperties">D2D1::RadialGradientBrushProperties</a>



<a href="/windows/win32/Direct2D/how-to-create-a-radial-gradient-brush">How to Create a Radial Gradient Brush</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>

