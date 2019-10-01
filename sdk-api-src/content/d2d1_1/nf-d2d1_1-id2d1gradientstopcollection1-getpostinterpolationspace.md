---
UID: NF:d2d1_1.ID2D1GradientStopCollection1.GetPostInterpolationSpace
title: ID2D1GradientStopCollection1::GetPostInterpolationSpace (d2d1_1.h)
author: windows-sdk-content
description: Gets the color space after interpolation has occurred.
old-location: direct2d\id2d1gradientstopcollection1_getpostinterpolationspace.htm
tech.root: Direct2D
ms.assetid: fb579d25-f38c-4f26-a29b-c6875cbabb3b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPostInterpolationSpace, GetPostInterpolationSpace method [Direct2D], GetPostInterpolationSpace method [Direct2D],ID2D1GradientStopCollection1 interface, ID2D1GradientStopCollection1 interface [Direct2D],GetPostInterpolationSpace method, ID2D1GradientStopCollection1.GetPostInterpolationSpace, ID2D1GradientStopCollection1::GetPostInterpolationSpace, d2d1_1/ID2D1GradientStopCollection1::GetPostInterpolationSpace, direct2d.id2d1gradientstopcollection1_getpostinterpolationspace
ms.topic: method
f1_keywords: 
 - "d2d1_1/ID2D1GradientStopCollection1.GetPostInterpolationSpace"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1GradientStopCollection1.GetPostInterpolationSpace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1GradientStopCollection1::GetPostInterpolationSpace


## -description


Gets the color space after interpolation has occurred.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE</a></b>

This method returns the color space.




## -remarks



If you create using <a href="https://docs.microsoft.com/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)">ID2D1RenderTarget::CreateGradientStopCollection</a>, this method returns <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_color_space">D2D1_COLOR_SPACE_SRGB</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection">ID2D1DeviceContext::CreateGradientStopCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1">ID2D1GradientStopCollection1</a>



<a href="https://docs.microsoft.com/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)">ID2D1RenderTarget::CreateGradientStopCollection</a>
 

 

