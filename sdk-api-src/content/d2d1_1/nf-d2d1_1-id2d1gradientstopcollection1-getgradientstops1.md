---
UID: NF:d2d1_1.ID2D1GradientStopCollection1.GetGradientStops1
title: ID2D1GradientStopCollection1::GetGradientStops1 (d2d1_1.h)
description: Copies the gradient stops from the collection into memory.
helpviewer_keywords: ["GetGradientStops1","GetGradientStops1 method [Direct2D]","GetGradientStops1 method [Direct2D]","ID2D1GradientStopCollection1 interface","ID2D1GradientStopCollection1 interface [Direct2D]","GetGradientStops1 method","ID2D1GradientStopCollection1.GetGradientStops1","ID2D1GradientStopCollection1::GetGradientStops1","d2d1_1/ID2D1GradientStopCollection1::GetGradientStops1","direct2d.id2d1gradientstopcollection1_getgradientstops1"]
old-location: direct2d\id2d1gradientstopcollection1_getgradientstops1.htm
tech.root: Direct2D
ms.assetid: da3987a5-b40f-49eb-9930-0162cf64d6a9
ms.date: 12/05/2018
ms.keywords: GetGradientStops1, GetGradientStops1 method [Direct2D], GetGradientStops1 method [Direct2D],ID2D1GradientStopCollection1 interface, ID2D1GradientStopCollection1 interface [Direct2D],GetGradientStops1 method, ID2D1GradientStopCollection1.GetGradientStops1, ID2D1GradientStopCollection1::GetGradientStops1, d2d1_1/ID2D1GradientStopCollection1::GetGradientStops1, direct2d.id2d1gradientstopcollection1_getgradientstops1
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1GradientStopCollection1::GetGradientStops1
 - d2d1_1/ID2D1GradientStopCollection1::GetGradientStops1
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
 - ID2D1GradientStopCollection1.GetGradientStops1
---

# ID2D1GradientStopCollection1::GetGradientStops1


## -description

Copies the gradient stops from the collection into memory.

## -parameters

### -param gradientStops [out]

Type: <b><a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a>*</b>

When this method returns, contains a pointer to a one-dimensional array of <a href="/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> structures.

### -param gradientStopsCount

Type: <b>UINT</b>

The number of gradient stops to copy.

## -remarks

If the [ID2D1DeviceContext::CreateGradientStopCollection](./nf-d2d1_1-id2d1devicecontext-creategradientstopcollection.md), this method returns the same values specified in the creation method. If the <b>ID2D1GradientStopCollection1</b> object was created using <b>ID2D1RenderTarget::CreateGradientStopCollection</b>, the stops returned here will first be transformed into the gamma space specified by the <i>colorInterpolationGamma</i> parameter. See the <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection">ID2D1DeviceContext::CreateGradientStopCollection</a>  method for more info about color space and gamma space.

If <i>gradientStopsCount</i> is less than the number of gradient stops in the collection, the remaining gradient stops are omitted. If <i>gradientStopsCount</i> is larger than the number of gradient stops in the collection, the extra gradient stops are set to <b>NULL</b>. To obtain the number of gradient stops in the collection, use the <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1gradientstopcollection-getgradientstopcount">GetGradientStopCount</a> method.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection">ID2D1DeviceContext::CreateGradientStopCollection</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1">ID2D1GradientStopCollection1</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)">ID2D1RenderTarget::CreateGradientStopCollection</a>