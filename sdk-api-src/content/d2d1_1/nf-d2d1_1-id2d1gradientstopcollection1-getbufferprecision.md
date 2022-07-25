---
UID: NF:d2d1_1.ID2D1GradientStopCollection1.GetBufferPrecision
title: ID2D1GradientStopCollection1::GetBufferPrecision (d2d1_1.h)
description: Gets the precision of the gradient buffer.
helpviewer_keywords: ["GetBufferPrecision","GetBufferPrecision method [Direct2D]","GetBufferPrecision method [Direct2D]","ID2D1GradientStopCollection1 interface","ID2D1GradientStopCollection1 interface [Direct2D]","GetBufferPrecision method","ID2D1GradientStopCollection1.GetBufferPrecision","ID2D1GradientStopCollection1::GetBufferPrecision","d2d1_1/ID2D1GradientStopCollection1::GetBufferPrecision","direct2d.id2d1gradientstopcollection1_getbufferprecision"]
old-location: direct2d\id2d1gradientstopcollection1_getbufferprecision.htm
tech.root: Direct2D
ms.assetid: 6a59c903-0fa8-4d2c-b426-8d3c3410c6bd
ms.date: 12/05/2018
ms.keywords: GetBufferPrecision, GetBufferPrecision method [Direct2D], GetBufferPrecision method [Direct2D],ID2D1GradientStopCollection1 interface, ID2D1GradientStopCollection1 interface [Direct2D],GetBufferPrecision method, ID2D1GradientStopCollection1.GetBufferPrecision, ID2D1GradientStopCollection1::GetBufferPrecision, d2d1_1/ID2D1GradientStopCollection1::GetBufferPrecision, direct2d.id2d1gradientstopcollection1_getbufferprecision
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
 - ID2D1GradientStopCollection1::GetBufferPrecision
 - d2d1_1/ID2D1GradientStopCollection1::GetBufferPrecision
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
 - ID2D1GradientStopCollection1.GetBufferPrecision
---

# ID2D1GradientStopCollection1::GetBufferPrecision


## -description

Gets the precision of the gradient buffer.



## -returns

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_buffer_precision">D2D1_BUFFER_PRECISION</a></b>

The buffer precision of the gradient buffer.

## -remarks

If this object was created using <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)">ID2D1RenderTarget::CreateGradientStopCollection</a>, this method returns D2D1_BUFFER_PRECISION_8BPC_UNORM.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection">ID2D1DeviceContext::CreateGradientStopCollection</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1">ID2D1GradientStopCollection1</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)">ID2D1RenderTarget::CreateGradientStopCollection</a>
