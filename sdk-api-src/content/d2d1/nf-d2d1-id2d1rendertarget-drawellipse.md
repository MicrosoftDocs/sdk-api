---
UID: NF:d2d1.ID2D1RenderTarget.DrawEllipse
title: ID2D1RenderTarget::DrawEllipse (d2d1.h)
author: windows-sdk-content
description: Draws the outline of an ellipse with the specified dimensions and stroke.
old-location: direct2d\id2d1rendertarget_drawellipse.htm
tech.root: Direct2D
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawEllipse, DrawEllipse methods [Direct2D], ID2D1RenderTarget.DrawEllipse, ID2D1RenderTarget::DrawEllipse, d2d1/DrawEllipse, direct2d.id2d1rendertarget_drawellipse
ms.topic: method
f1_keywords: ["d2d1/ID2D1RenderTarget::DrawEllipse"]
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
 - ID2D1RenderTarget::DrawEllipse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::DrawEllipse


## -description


<span>Draws the outline of an ellipse with the specified dimensions and stroke.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)">DrawEllipse(D2D1_ELLIPSE&,ID2D1Brush*,FLOAT,ID2D1StrokeStyle*)</a>
</td>
<td align="left" width="63%">
Draws the outline of the specified ellipse using the specified stroke style.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)">DrawEllipse(D2D1_ELLIPSE*,ID2D1Brush*,FLOAT,ID2D1StrokeStyle*)</a>
</td>
<td align="left" width="63%">
Draws the outline of the specified ellipse using the specified stroke style.

</td>
</tr>
</table>

## -parameters


## -remarks



The <b>DrawEllipse</b> method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>DrawEllipse</b>) failed, check the result returned by the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-draw-an-ellipse">How to Draw and Fill a Basic Shape</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-fillellipse">FillEllipse</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

