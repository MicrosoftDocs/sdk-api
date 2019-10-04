---
UID: NF:d2d1.ID2D1RenderTarget.CreateGradientStopCollection(const D2D1_GRADIENT_STOP,UINT32,D2D1_GAMMA,D2D1_EXTEND_MODE,ID2D1GradientStopCollection)
title: ID2D1RenderTarget::CreateGradientStopCollection (d2d1.h)
author: windows-sdk-content
description: Creates an ID2D1GradientStopCollection from the specified array of D2D1_GRADIENT_STOP structures.
old-location: direct2d\id2d1rendertarget_creategradientstopcollection.htm
tech.root: Direct2D
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateGradientStopCollection, CreateGradientStopCollection methods [Direct2D], ID2D1RenderTarget.CreateGradientStopCollection, ID2D1RenderTarget::CreateGradientStopCollection, d2d1_1/CreateGradientStopCollection, direct2d.id2d1rendertarget_creategradientstopcollection
ms.topic: method
f1_keywords: 
 - "d2d1/ID2D1RenderTarget::CreateGradientStopCollection"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget::CreateGradientStopCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::CreateGradientStopCollection


## -description


<span>     Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a> from the specified array of <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> structures. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)">CreateGradientStopCollection(D2D1_GRADIENT_STOP*,D2D1_GAMMA,D2D1_EXTEND_MODE,ID2D1GradientStopCollection**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a> from the specified gradient stops, color interpolation gamma, and extend mode.  

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)">CreateGradientStopCollection(D2D1_GRADIENT_STOP*,ID2D1GradientStopCollection**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a> from the specified gradient stops that uses the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_gamma">D2D1_GAMMA_2_2</a> color interpolation gamma and the clamp extend mode.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-create-a-linear-gradient-brush">How to Create a Linear Gradient Brush</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-create-a-radial-gradient-brush">How to Create a Radial Gradient Brush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

