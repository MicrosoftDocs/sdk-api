---
UID: NF:d2d1.ID2D1RenderTarget.CreateGradientStopCollection(constD2D1_GRADIENT_STOP,UINT32,D2D1_GAMMA,D2D1_EXTEND_MODE,ID2D1GradientStopCollection)
title: ID2D1RenderTarget::CreateGradientStopCollection (d2d1.h)
description: Creates an ID2D1GradientStopCollection from the specified array of D2D1_GRADIENT_STOP structures.
helpviewer_keywords: ["CreateGradientStopCollection","CreateGradientStopCollection methods [Direct2D]","ID2D1RenderTarget.CreateGradientStopCollection","ID2D1RenderTarget::CreateGradientStopCollection","d2d1_1/CreateGradientStopCollection","direct2d.id2d1rendertarget_creategradientstopcollection"]
old-location: direct2d\id2d1rendertarget_creategradientstopcollection.htm
tech.root: Direct2D
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
ms.date: 12/05/2018
ms.keywords: CreateGradientStopCollection, CreateGradientStopCollection methods [Direct2D], ID2D1RenderTarget.CreateGradientStopCollection, ID2D1RenderTarget::CreateGradientStopCollection, d2d1_1/CreateGradientStopCollection, direct2d.id2d1rendertarget_creategradientstopcollection
req.header: d2d1.h
req.include-header: D2d1.h
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
 - ID2D1RenderTarget::CreateGradientStopCollection
 - d2d1/ID2D1RenderTarget::CreateGradientStopCollection
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
 - ID2D1RenderTarget::CreateGradientStopCollection
---

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a> from the specified array of <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> structures.

## -parameters

### -param gradientStops

Type: [in] <b><a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a>*</b>

A pointer to an array of <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> structures.

### -param gradientStopsCount

Type: [in] <b>UINT</b>

A value greater than or equal to 1 that specifies the number of gradient stops in the <i>gradientStops</i> array.

### -param colorInterpolationGamma

Type: [in] <b>D2D1_GAMMA</b>

The space in which color interpolation between the gradient stops is performed.

### -param extendMode

Type: [in] <b>D2D1_EXTEND_MODE</b>

The behavior of the gradient outside the [0,1] normalized range.

### -param gradientStopCollection

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>**</b>

When this method returns, contains a pointer to a pointer to the new gradient stop collection.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>

<a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a>

<a href="/windows/win32/Direct2D/how-to-create-a-linear-gradient-brush">How to Create a Linear Gradient Brush</a>

<a href="/windows/win32/Direct2D/how-to-create-a-radial-gradient-brush">How to Create a Radial Gradient Brush</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

