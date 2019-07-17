---
UID: NN:d2d1_1.ID2D1GradientStopCollection1
title: ID2D1GradientStopCollection1 (d2d1_1.h)
author: windows-sdk-content
description: Represents a collection of D2D1_GRADIENT_STOP objects for linear and radial gradient brushes. It provides get methods for all the new parameters added to the gradient stop collection.
old-location: direct2d\id2d1gradientstopcollection1.htm
tech.root: Direct2D
ms.assetid: aa423e18-c6b5-4587-b044-deda00a84615
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1GradientStopCollection1, ID2D1GradientStopCollection1 interface [Direct2D], ID2D1GradientStopCollection1 interface [Direct2D],described, d2d1_1/ID2D1GradientStopCollection1, direct2d.id2d1gradientstopcollection1
ms.topic: interface
f1_keywords: 
 - "d2d1_1/ID2D1GradientStopCollection1"
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
 - ID2D1GradientStopCollection1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1GradientStopCollection1 interface


## -description


Represents a collection of <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop">D2D1_GRADIENT_STOP</a> objects for linear and radial gradient brushes. It provides get methods for all the new parameters added to the gradient stop collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1GradientStopCollection1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>. <b>ID2D1GradientStopCollection1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1GradientStopCollection1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gradientstopcollection1-getbufferprecision">GetBufferPrecision</a>
</td>
<td align="left" width="63%">
Gets the precision of the gradient buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gradientstopcollection1-getcolorinterpolationmode">GetColorInterpolationMode</a>
</td>
<td align="left" width="63%">
Retrieves the color interpolation mode that the gradient stop collection uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gradientstopcollection1-getgradientstops1">GetGradientStops1</a>
</td>
<td align="left" width="63%">
Copies the gradient stops from the collection into memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gradientstopcollection1-getpostinterpolationspace">GetPostInterpolationSpace</a>
</td>
<td align="left" width="63%">
Gets the color space after interpolation has occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gradientstopcollection1-getpreinterpolationspace">GetPreInterpolationSpace</a>
</td>
<td align="left" width="63%">
Gets the color space of the input colors as well as the space in which gradient stops are interpolated.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection">ID2D1DeviceContext::CreateGradientStopCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1gradientstopcollection">ID2D1GradientStopCollection</a>



<a href="https://docs.microsoft.com/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection">ID2D1RenderTarget::CreateGradientStopCollection</a>
 

 

