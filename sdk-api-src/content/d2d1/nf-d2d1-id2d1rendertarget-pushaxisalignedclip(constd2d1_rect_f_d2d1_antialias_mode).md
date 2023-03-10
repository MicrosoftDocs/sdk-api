---
UID: NF:d2d1.ID2D1RenderTarget.PushAxisAlignedClip(constD2D1_RECT_F,D2D1_ANTIALIAS_MODE)
title: ID2D1RenderTarget::PushAxisAlignedClip (d2d1.h)
description: Specifies a rectangle to which all subsequent drawing operations are clipped. (overload 1/2)
helpviewer_keywords: ["ID2D1RenderTarget.PushAxisAlignedClip","ID2D1RenderTarget::PushAxisAlignedClip","PushAxisAlignedClip","PushAxisAlignedClip methods [Direct2D]","d2d1_1/PushAxisAlignedClip","direct2d.id2d1rendertarget_pushaxisalignedclip"]
old-location: direct2d\id2d1rendertarget_pushaxisalignedclip.htm
tech.root: Direct2D
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget.PushAxisAlignedClip, ID2D1RenderTarget::PushAxisAlignedClip, PushAxisAlignedClip, PushAxisAlignedClip methods [Direct2D], d2d1_1/PushAxisAlignedClip, direct2d.id2d1rendertarget_pushaxisalignedclip
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1RenderTarget::PushAxisAlignedClip
 - d2d1/ID2D1RenderTarget::PushAxisAlignedClip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget::PushAxisAlignedClip
---

## -description

Specifies a rectangle to which all subsequent drawing operations are clipped.

## -parameters

### -param clipRect

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The size and position of the clipping area, in device-independent pixels.

### -param antialiasMode

Type: [in] <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode that is used to draw the edges of clip rects that have subpixel boundaries, and to blend the clip with the scene contents. The blending is performed once when the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip">PopAxisAlignedClip</a> method is called, and does not apply to each primitive within the layer.

## -remarks

The <i>clipRect</i> is transformed by the current world transform set on the render target. After the transform is applied to the <i>clipRect</i> that is passed in, the axis-aligned bounding box for the <i>clipRect</i> is computed. For efficiency, the contents are clipped to this axis-aligned bounding box and not to the original <i>clipRect</i> that is passed in. 

The following diagrams show how a rotation transform is applied to the render target, the resulting <i>clipRect</i>, and a calculated axis-aligned bounding box.

<ol>
<li>
Assume the rectangle in the following illustration is a render target that is aligned to the screen pixels.

<img alt="Illustration of a rectangle (render target)" src="images/pushaxisalignedclip_step1_rendertarget.png"/>

</li>
<li>
Apply a rotation transform to the render target. In the following illustration, the black rectangle represents the original render target and the red dashed rectangle represents the transformed render target.

<img alt="Illustration of a rotated rectangle (transformed render target)" src="images/pushaxisalignedclip_step2_transformed.png"/>

</li>
<li>
After calling <b>PushAxisAlignedClip</b>, the rotation transform is applied to the <i>clipRect</i>. In the following illustration, the blue rectangle represents the transformed <i>clipRect</i>.

<img alt="Illustration of a small blue rectangle (transformed clipRect) inside a rotated rectangle" src="images/pushaxisalignedclip_step3_clipRecttransformed.png"/>

</li>
<li>
The axis-aligned bounding box is calculated. The green dashed rectangle represents the bounding box in the following illustration. All contents are clipped to this axis-aligned bounding box.

<img alt="Illustration of a green bounding box around a small blue rectangle inside a rotated rectangle" src="images/pushaxisalignedclip_step4_boundingbox.png"/>

</li>
</ol>
<div class="alert"><b>Note</b>  If rendering operations fail or if <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip">PopAxisAlignedClip</a> is not called, clip rects may cause some artifacts on the render target. <b>PopAxisAlignedClip</b> can be considered a drawing operation that is designed to fix the borders of a clipping region. Without this call, the borders of a clipped area may be not antialiased or otherwise corrected.</div>
<div> </div>
The <b>PushAxisAlignedClip</b> and <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip">PopAxisAlignedClip</a> must match. Otherwise, the error state is set. For the render target to continue receiving new commands, you can call <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">Flush</a> to clear the error. 

A <b>PushAxisAlignedClip</b> and <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)">PopAxisAlignedClip</a> pair can occur around or within a PushLayer and PopLayer, but cannot overlap. For example, the sequence of <b>PushAxisAlignedClip</b>, <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a>, <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a>, <b>PopAxisAlignedClip</b> is valid, but the sequence of <b>PushAxisAlignedClip</b>, <b>PushLayer</b>, <b>PopAxisAlignedClip</b>, <b>PopLayer</b> is invalid.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)">PushAxisAlignedClip</a>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

