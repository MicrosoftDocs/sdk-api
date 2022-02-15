---
UID: NF:d2d1_1.ID2D1GradientStopCollection1.GetPreInterpolationSpace
title: ID2D1GradientStopCollection1::GetPreInterpolationSpace (d2d1_1.h)
description: Gets the color space of the input colors as well as the space in which gradient stops are interpolated.
helpviewer_keywords: ["GetPreInterpolationSpace","GetPreInterpolationSpace method [Direct2D]","GetPreInterpolationSpace method [Direct2D]","ID2D1GradientStopCollection1 interface","ID2D1GradientStopCollection1 interface [Direct2D]","GetPreInterpolationSpace method","ID2D1GradientStopCollection1.GetPreInterpolationSpace","ID2D1GradientStopCollection1::GetPreInterpolationSpace","d2d1_1/ID2D1GradientStopCollection1::GetPreInterpolationSpace","direct2d.id2d1gradientstopcollection1_getpreinterpolationspace"]
old-location: direct2d\id2d1gradientstopcollection1_getpreinterpolationspace.htm
tech.root: Direct2D
ms.assetid: 8222d713-c47e-4e4c-92aa-040dc9085ce9
ms.date: 12/05/2018
ms.keywords: GetPreInterpolationSpace, GetPreInterpolationSpace method [Direct2D], GetPreInterpolationSpace method [Direct2D],ID2D1GradientStopCollection1 interface, ID2D1GradientStopCollection1 interface [Direct2D],GetPreInterpolationSpace method, ID2D1GradientStopCollection1.GetPreInterpolationSpace, ID2D1GradientStopCollection1::GetPreInterpolationSpace, d2d1_1/ID2D1GradientStopCollection1::GetPreInterpolationSpace, direct2d.id2d1gradientstopcollection1_getpreinterpolationspace
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
 - ID2D1GradientStopCollection1::GetPreInterpolationSpace
 - d2d1_1/ID2D1GradientStopCollection1::GetPreInterpolationSpace
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
 - ID2D1GradientStopCollection1.GetPreInterpolationSpace
---

# ID2D1GradientStopCollection1::GetPreInterpolationSpace


## -description

Gets the color space of the input colors as well as the space in which gradient stops are interpolated.



## -returns

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a></b>

This method returns the color space.

## -remarks

If this object was created using <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)">ID2D1RenderTarget::CreateGradientStopCollection</a>, this method  returns the color space related to the color interpolation gamma.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection">ID2D1DeviceContext::CreateGradientStopCollection</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1">ID2D1GradientStopCollection1</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)">ID2D1RenderTarget::CreateGradientStopCollection</a>
