---
UID: NF:d2d1.ID2D1RenderTarget.FillEllipse(const D2D1_ELLIPSE,ID2D1Brush)
title: ID2D1RenderTarget::FillEllipse (d2d1.h)
author: windows-sdk-content
description: Paints the interior of the specified ellipse.
old-location: direct2d\id2d1rendertarget_fillellipse.htm
tech.root: Direct2D
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FillEllipse, FillEllipse methods [Direct2D], ID2D1RenderTarget.FillEllipse, ID2D1RenderTarget::FillEllipse, d2d1/FillEllipse, direct2d.id2d1rendertarget_fillellipse
ms.topic: method
f1_keywords: 
 - "d2d1/ID2D1RenderTarget::FillEllipse"
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
 - ID2D1RenderTarget::FillEllipse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::FillEllipse


## -description


<span>Paints the interior of the specified ellipse.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)">FillEllipse(D2D1_ELLIPSE&,ID2D1Brush*)</a>
</td>
<td align="left" width="63%">
Paints the interior of the specified ellipse.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)">FillEllipse(D2D1_ELLIPSE*,ID2D1Brush*)</a>
</td>
<td align="left" width="63%">
Paints the interior of the specified ellipse.

</td>
</tr>
</table>

## -parameters


## -remarks



This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>FillEllipse</b>) failed, check the result returned by the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-draw-an-ellipse">How to Draw and Fill a Basic Shape</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-draw-an-ellipse">How to Draw and Fill a Basic Shape</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

