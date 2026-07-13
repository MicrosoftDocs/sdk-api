---
UID: NF:d2d1.ID2D1RenderTarget.PopAxisAlignedClip
title: ID2D1RenderTarget::PopAxisAlignedClip (d2d1.h)
description: Removes the last axis-aligned clip from the render target. After this method is called, the clip is no longer applied to subsequent drawing operations.
helpviewer_keywords: ["ID2D1RenderTarget interface [Direct2D]","PopAxisAlignedClip method","ID2D1RenderTarget.PopAxisAlignedClip","ID2D1RenderTarget::PopAxisAlignedClip","PopAxisAlignedClip","PopAxisAlignedClip method [Direct2D]","PopAxisAlignedClip method [Direct2D]","ID2D1RenderTarget interface","d2d1/ID2D1RenderTarget::PopAxisAlignedClip","direct2d.ID2D1RenderTarget_PopAxisAlignedClip"]
old-location: direct2d\ID2D1RenderTarget_PopAxisAlignedClip.htm
tech.root: Direct2D
ms.assetid: 0f0a2826-2356-4ced-a372-5bb59dd394ee
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],PopAxisAlignedClip method, ID2D1RenderTarget.PopAxisAlignedClip, ID2D1RenderTarget::PopAxisAlignedClip, PopAxisAlignedClip, PopAxisAlignedClip method [Direct2D], PopAxisAlignedClip method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::PopAxisAlignedClip, direct2d.ID2D1RenderTarget_PopAxisAlignedClip
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - ID2D1RenderTarget::PopAxisAlignedClip
 - d2d1/ID2D1RenderTarget::PopAxisAlignedClip
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
 - ID2D1RenderTarget.PopAxisAlignedClip
---

# ID2D1RenderTarget::PopAxisAlignedClip


## -description

Removes the last axis-aligned clip from the render target. After this method is called, the clip is no longer applied to subsequent drawing operations.



## -remarks

A <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)">PushAxisAlignedClip</a>/<b>PopAxisAlignedClip</b> pair can occur around or within a <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)">PushLayer</a>/<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer">PopLayer</a> pair, but may not overlap. For example, a <b>PushAxisAlignedClip</b>, <b>PushLayer</b>, <b>PopLayer</b>, <b>PopAxisAlignedClip</b>  sequence is valid, but a <b>PushAxisAlignedClip</b>, <b>PushLayer</b>, <b>PopAxisAlignedClip</b>, <b>PopLayer</b> sequence is not. 

<b>PopAxisAlignedClip</b> must be called once for every call to <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)">PushAxisAlignedClip</a>.

For an example, see <a href="/windows/win32/Direct2D/how-to-clip-with-axis-aligned-rects">How to Clip with an Axis-Aligned Clip Rectangle</a>.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>PopAxisAlignedClip</b>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

