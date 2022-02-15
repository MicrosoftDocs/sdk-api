---
UID: NF:d2d1.ID2D1RenderTarget.CreateRadialGradientBrush(constD2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES&,ID2D1GradientStopCollection,ID2D1RadialGradientBrush)
title: ID2D1RenderTarget::CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush) (d2d1.h)
description: Creates an ID2D1RadialGradientBrush that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.
helpviewer_keywords: ["CreateRadialGradientBrush","CreateRadialGradientBrush method [Direct2D]","CreateRadialGradientBrush method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateRadialGradientBrush method","ID2D1RenderTarget.CreateRadialGradientBrush","ID2D1RenderTarget.CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &","ID2D1GradientStopCollection","ID2D1RadialGradientBrush)","ID2D1RenderTarget::CreateRadialGradientBrush","ID2D1RenderTarget::CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &","ID2D1GradientStopCollection","ID2D1RadialGradientBrush)","d2d1/ID2D1RenderTarget::CreateRadialGradientBrush","direct2d.ID2D1RenderTarget_CreateRadialGradientBrush_overload2","direct2d.ID2D1RenderTarget_CreateRadialGradientBrush_ref_D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES_ptr_ID2D1GradientStopCollection_ptr_ptr_ID2D1RadialGradientBrush"]
old-location: direct2d\ID2D1RenderTarget_CreateRadialGradientBrush_overload2.htm
tech.root: Direct2D
ms.assetid: 177d0b8c-82ae-4d2a-ae43-246352b92166
ms.date: 12/05/2018
ms.keywords: CreateRadialGradientBrush, CreateRadialGradientBrush method [Direct2D], CreateRadialGradientBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateRadialGradientBrush method, ID2D1RenderTarget.CreateRadialGradientBrush, ID2D1RenderTarget.CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush), ID2D1RenderTarget::CreateRadialGradientBrush, ID2D1RenderTarget::CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush), d2d1/ID2D1RenderTarget::CreateRadialGradientBrush, direct2d.ID2D1RenderTarget_CreateRadialGradientBrush_overload2, direct2d.ID2D1RenderTarget_CreateRadialGradientBrush_ref_D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES_ptr_ID2D1GradientStopCollection_ptr_ptr_ID2D1RadialGradientBrush
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
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.CreateRadialGradientBrush
---

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a> that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.

## -parameters

### -param radialGradientBrushProperties

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties">D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES</a> &</b>

The center, gradient origin offset, and x-radius and y-radius of the brush's gradient.

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

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

