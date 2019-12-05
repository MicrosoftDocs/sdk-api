---
UID: NF:d2d1.ID2D1RenderTarget.PushAxisAlignedClip(const D2D1_RECT_F,D2D1_ANTIALIAS_MODE)
title: ID2D1RenderTarget::PushAxisAlignedClip (d2d1.h)
description: Specifies a rectangle to which all subsequent drawing operations are clipped.
old-location: direct2d\id2d1rendertarget_pushaxisalignedclip.htm
tech.root: Direct2D
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget.PushAxisAlignedClip, ID2D1RenderTarget::PushAxisAlignedClip, PushAxisAlignedClip, PushAxisAlignedClip methods [Direct2D], d2d1_1/PushAxisAlignedClip, direct2d.id2d1rendertarget_pushaxisalignedclip
ms.topic: method
f1_keywords:
- d2d1/ID2D1RenderTarget::PushAxisAlignedClip
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
- ID2D1RenderTarget::PushAxisAlignedClip
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::PushAxisAlignedClip


## -description


<span>Specifies a rectangle to which all subsequent drawing operations are clipped.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)">PushAxisAlignedClip(D2D1_RECT_F&,D2D1_ANTIALIAS_MODE)</a>
</td>
<td align="left" width="63%">
Specifies a rectangle to which all subsequent drawing operations are clipped.
    

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)">PushAxisAlignedClip(D2D1_RECT_F*,D2D1_ANTIALIAS_MODE)</a>
</td>
<td align="left" width="63%">
Specifies a rectangle to which all subsequent drawing operations are clipped.

</td>
</tr>
</table>

## -parameters


## -remarks



A           [PushLayer](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))a> and <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a>, but cannot overlap. For example, the sequence of <b>PushAxisAlignedClip</b>, <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a>, <b>PopLayer</b>, <b>PopAxisAlignedClip</b> is valid, but the sequence of <b>PushAxisAlignedClip</b>, <b>PushLayer</b>, <b>PopAxisAlignedClip</b>, <b>PopLayer</b> is invalid.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>PushAxisAlignedClip</b>) failed, check the result returned by the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

For an example, see the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-clip-with-axis-aligned-rects">How to Clip with an Axis-Aligned Clip Rectangle</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

