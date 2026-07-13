---
UID: NF:d2d1.ID2D1RenderTarget.CreateRadialGradientBrush(constD2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES,constD2D1_BRUSH_PROPERTIES,ID2D1GradientStopCollection,ID2D1RadialGradientBrush)
title: ID2D1RenderTarget::CreateRadialGradientBrush (d2d1.h)
description: Creates an ID2D1RadialGradientBrush object that can be used to paint areas with a radial gradient.
helpviewer_keywords: ["CreateRadialGradientBrush","CreateRadialGradientBrush methods [Direct2D]","ID2D1RenderTarget.CreateRadialGradientBrush","ID2D1RenderTarget::CreateRadialGradientBrush","d2d1/CreateRadialGradientBrush","direct2d.id2d1rendertarget_createradialgradientbrush"]
old-location: direct2d\id2d1rendertarget_createradialgradientbrush.htm
tech.root: Direct2D
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
ms.date: 12/05/2018
ms.keywords: CreateRadialGradientBrush, CreateRadialGradientBrush methods [Direct2D], ID2D1RenderTarget.CreateRadialGradientBrush, ID2D1RenderTarget::CreateRadialGradientBrush, d2d1/CreateRadialGradientBrush, direct2d.id2d1rendertarget_createradialgradientbrush
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ID2D1RenderTarget::CreateRadialGradientBrush
 - d2d1/ID2D1RenderTarget::CreateRadialGradientBrush
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
 - ID2D1RenderTarget::CreateRadialGradientBrush
---

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a> object that can be used to paint areas with a radial gradient.

## -parameters

### -param radialGradientBrushProperties

Type: <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties">D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES</a>*</b>

The center, gradient origin offset, and x-radius and y-radius of the brush's gradient.

### -param brushProperties

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties">D2D1_BRUSH_PROPERTIES</a>*</b>

The transform and base opacity of the new brush.

### -param gradientStopCollection

Type: [in] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>*</b>

A collection of <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> structures that describe the colors in the brush's gradient and their locations along the gradient.

### -param radialGradientBrush

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>**</b>

When this method returns, contains a pointer to a pointer to the new brush. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>

<a href="/windows/win32/Direct2D/how-to-create-a-radial-gradient-brush">How to Create a Radial Gradient Brush</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

