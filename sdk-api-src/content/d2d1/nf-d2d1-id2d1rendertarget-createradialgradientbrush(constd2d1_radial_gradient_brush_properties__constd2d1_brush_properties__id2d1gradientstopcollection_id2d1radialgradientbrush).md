---
UID: NF:d2d1.ID2D1RenderTarget.CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush)
title: ID2D1RenderTarget::CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush) (d2d1.h)
description: Creates an ID2D1RadialGradientBrush that contains the specified gradient stops and has the specified transform and base opacity.helpviewer_keywords: ["CreateRadialGradientBrush","CreateRadialGradientBrush method [Direct2D]","CreateRadialGradientBrush method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateRadialGradientBrush method","ID2D1RenderTarget.CreateRadialGradientBrush","ID2D1RenderTarget.CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &","const D2D1_BRUSH_PROPERTIES &","ID2D1GradientStopCollection","ID2D1RadialGradientBrush)","ID2D1RenderTarget::CreateRadialGradientBrush","ID2D1RenderTarget::CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &","const D2D1_BRUSH_PROPERTIES &","ID2D1GradientStopCollection","ID2D1RadialGradientBrush)","d2d1/ID2D1RenderTarget::CreateRadialGradientBrush","direct2d.ID2D1RenderTarget_CreateRadialGradientBrush_overload1","direct2d.ID2D1RenderTarget_CreateRadialGradientBrush_ref_D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES_ref_D2D1_BRUSH_PROPERTIES_ptr_ID2D1GradientStopCollection_ptr_ptr_ID2D1RadialGradientBrush"]
old-location: direct2d\ID2D1RenderTarget_CreateRadialGradientBrush_overload1.htm
tech.root: Direct2D
ms.assetid: df87e288-392d-439e-8d03-e4866fde892f
ms.date: 12/05/2018
ms.keywords: CreateRadialGradientBrush, CreateRadialGradientBrush method [Direct2D], CreateRadialGradientBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateRadialGradientBrush method, ID2D1RenderTarget.CreateRadialGradientBrush, ID2D1RenderTarget.CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush), ID2D1RenderTarget::CreateRadialGradientBrush, ID2D1RenderTarget::CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush), d2d1/ID2D1RenderTarget::CreateRadialGradientBrush, direct2d.ID2D1RenderTarget_CreateRadialGradientBrush_overload1, direct2d.ID2D1RenderTarget_CreateRadialGradientBrush_ref_D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES_ref_D2D1_BRUSH_PROPERTIES_ptr_ID2D1GradientStopCollection_ptr_ptr_ID2D1RadialGradientBrush
f1_keywords:
- d2d1/ID2D1RenderTarget.CreateRadialGradientBrush
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1RenderTarget.CreateRadialGradientBrush
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::CreateRadialGradientBrush(const D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1RadialGradientBrush)


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a> that contains the specified gradient stops and has the specified transform and base opacity.


## -parameters




### -param radialGradientBrushProperties [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties">D2D1_RADIAL_GRADIENT_BRUSH_PROPERTIES</a></b>

The center, gradient origin offset, and x-radius and y-radius of the brush's gradient.


### -param brushProperties [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties">D2D1_BRUSH_PROPERTIES</a></b>

The transform and base opacity of the new brush.


### -param gradientStopCollection [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>*</b>

A collection of <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> structures that describe the colors in the brush's gradient and their locations along the gradient.


### -param radialGradientBrush [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>**</b>

When this method returns, contains a pointer to a pointer to the new brush. This parameter is passed uninitialized.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-create-a-radial-gradient-brush">How to Create a Radial Gradient Brush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

