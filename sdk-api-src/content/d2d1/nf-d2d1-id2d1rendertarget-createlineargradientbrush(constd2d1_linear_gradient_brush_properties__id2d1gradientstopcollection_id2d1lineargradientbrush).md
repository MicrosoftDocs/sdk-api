---
UID: NF:d2d1.ID2D1RenderTarget.CreateLinearGradientBrush(constD2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES&,ID2D1GradientStopCollection,ID2D1LinearGradientBrush)
title: ID2D1RenderTarget::CreateLinearGradientBrush(const D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1LinearGradientBrush) (d2d1.h)
description: Creates an ID2D1LinearGradientBrush that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.
helpviewer_keywords: ["CreateLinearGradientBrush","CreateLinearGradientBrush method [Direct2D]","CreateLinearGradientBrush method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateLinearGradientBrush method","ID2D1RenderTarget.CreateLinearGradientBrush","ID2D1RenderTarget.CreateLinearGradientBrush(const D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES &","ID2D1GradientStopCollection","ID2D1LinearGradientBrush)","ID2D1RenderTarget::CreateLinearGradientBrush","ID2D1RenderTarget::CreateLinearGradientBrush(const D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES &","ID2D1GradientStopCollection","ID2D1LinearGradientBrush)","d2d1/ID2D1RenderTarget::CreateLinearGradientBrush","direct2d.ID2D1RenderTarget_CreateLinearGradientBrush_overload2","direct2d.ID2D1RenderTarget_CreateLinearGradientBrush_ref_D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES_ptr_ID2D1GradientStopCollection_ptr_ptr_ID2D1LinearGradientBrush"]
old-location: direct2d\ID2D1RenderTarget_CreateLinearGradientBrush_overload2.htm
tech.root: Direct2D
ms.assetid: b13314ca-3b0b-4d51-99cc-0a56eae223f1
ms.date: 12/05/2018
ms.keywords: CreateLinearGradientBrush, CreateLinearGradientBrush method [Direct2D], CreateLinearGradientBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateLinearGradientBrush method, ID2D1RenderTarget.CreateLinearGradientBrush, ID2D1RenderTarget.CreateLinearGradientBrush(const D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1LinearGradientBrush), ID2D1RenderTarget::CreateLinearGradientBrush, ID2D1RenderTarget::CreateLinearGradientBrush(const D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES &,ID2D1GradientStopCollection,ID2D1LinearGradientBrush), d2d1/ID2D1RenderTarget::CreateLinearGradientBrush, direct2d.ID2D1RenderTarget_CreateLinearGradientBrush_overload2, direct2d.ID2D1RenderTarget_CreateLinearGradientBrush_ref_D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES_ptr_ID2D1GradientStopCollection_ptr_ptr_ID2D1LinearGradientBrush
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
 - ID2D1RenderTarget::CreateLinearGradientBrush
 - d2d1/ID2D1RenderTarget::CreateLinearGradientBrush
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
 - ID2D1RenderTarget.CreateLinearGradientBrush
---

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a> that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.

## -parameters

### -param linearGradientBrushProperties

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties">D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES</a> &</b>

The start and end points of the gradient.

### -param gradientStopCollection

Type: [in] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>*</b>

A collection of <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> structures that describe the colors in the brush's gradient and their locations along the gradient line.

### -param linearGradientBrush

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a>**</b>

When this method returns, contains the address of a pointer to the new brush. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>

<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)">CreateGradientStopCollection</a>

<a href="/windows/win32/Direct2D/how-to-create-a-linear-gradient-brush">How to Create a Linear Gradient Brush</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

