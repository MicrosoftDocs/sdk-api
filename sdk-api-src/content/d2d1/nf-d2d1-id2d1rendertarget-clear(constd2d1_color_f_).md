---
UID: NF:d2d1.ID2D1RenderTarget.Clear(constD2D1_COLOR_F&)
title: ID2D1RenderTarget::Clear(const D2D1_COLOR_F &) (d2d1.h)
description: Clears the drawing area to the specified color. (overload 2/3)
helpviewer_keywords: ["Clear","Clear method [Direct2D]","Clear method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","Clear method","ID2D1RenderTarget.Clear","ID2D1RenderTarget.Clear(const D2D1_COLOR_F &)","ID2D1RenderTarget::Clear","ID2D1RenderTarget::Clear(const D2D1_COLOR_F &)","ID2D1RenderTarget::Clear(const D2D1_COLOR_F)","d2d1/ID2D1RenderTarget::Clear","direct2d.ID2D1RenderTarget_Clear_ptr_COLOR_F"]
old-location: direct2d\ID2D1RenderTarget_Clear_ptr_COLOR_F.htm
tech.root: Direct2D
ms.assetid: c39b83e0-4cde-4e94-94e9-37b5c36f7877
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [Direct2D], Clear method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],Clear method, ID2D1RenderTarget.Clear, ID2D1RenderTarget.Clear(const D2D1_COLOR_F &), ID2D1RenderTarget::Clear, ID2D1RenderTarget::Clear(const D2D1_COLOR_F &), ID2D1RenderTarget::Clear(const D2D1_COLOR_F), d2d1/ID2D1RenderTarget::Clear, direct2d.ID2D1RenderTarget_Clear_ptr_COLOR_F
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
 - ID2D1RenderTarget::Clear
 - d2d1/ID2D1RenderTarget::Clear
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
 - ID2D1RenderTarget.Clear
---

## -description

Clears the drawing area to the specified color.

## -parameters

### -param clearColor

Type: [in] <b>const <a href="/windows/win32/Direct2D/d2d1-color-f">D2D1_COLOR_F</a> &</b>

The color to which the drawing area is cleared.

## -remarks

Direct2D interprets the <i>clearColor</i> as straight alpha (not premultiplied).  If the render target's alpha mode is <a href="/windows/win32/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_IGNORE</a>, the alpha channel of <i>clearColor</i> is ignored and replaced with 1.0f (fully opaque).

If the render target has an active clip (specified by <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)">PushAxisAlignedClip</a>), the clear command is applied only to the area within the clip region.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

