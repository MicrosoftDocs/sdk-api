---
UID: NF:d2d1.ID2D1RenderTarget.CreateLinearGradientBrush(const D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES,const D2D1_BRUSH_PROPERTIES,ID2D1GradientStopCollection,ID2D1LinearGradientBrush)
title: ID2D1RenderTarget::CreateLinearGradientBrush (d2d1.h)

description: Creates an ID2D1LinearGradientBrush object for painting areas with a linear gradient.
old-location: direct2d\id2d1rendertarget_createlineargradientbrush.htm
tech.root: Direct2D
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0

ms.date: 12/05/2018
ms.keywords: CreateLinearGradientBrush, CreateLinearGradientBrush methods [Direct2D], ID2D1RenderTarget.CreateLinearGradientBrush, ID2D1RenderTarget::CreateLinearGradientBrush, d2d1/CreateLinearGradientBrush, direct2d.id2d1rendertarget_createlineargradientbrush
ms.topic: method
f1_keywords: 
 - "d2d1/ID2D1RenderTarget::CreateLinearGradientBrush"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget::CreateLinearGradientBrush
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::CreateLinearGradientBrush


## -description


<span>Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a> object for painting areas with a linear gradient.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)">CreateLinearGradientBrush(D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES&,ID2D1GradientStopCollection*,ID2D1LinearGradientBrush**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a> that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.
    

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)">CreateLinearGradientBrush(D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES&,D2D1_BRUSH_PROPERTIES&,ID2D1GradientStopCollection*,ID2D1LinearGradientBrush**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a> that contains the specified gradient stops and has the specified transform and base opacity.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)">CreateLinearGradientBrush(D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES*,D2D1_BRUSH_PROPERTIES*,ID2D1GradientStopCollection*,ID2D1LinearGradientBrush**)</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a> that contains the specified gradient stops and has the specified transform and base opacity.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="https://docs.microsoft.com/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)">CreateGradientStopCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-create-a-linear-gradient-brush">How to Create a Linear Gradient Brush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1lineargradientbrush">ID2D1LinearGradientBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1radialgradientbrush">ID2D1RadialGradientBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

