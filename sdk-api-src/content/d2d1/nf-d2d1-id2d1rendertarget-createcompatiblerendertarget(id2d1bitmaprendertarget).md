---
UID: NF:d2d1.ID2D1RenderTarget.CreateCompatibleRenderTarget(ID2D1BitmapRenderTarget)
title: ID2D1RenderTarget::CreateCompatibleRenderTarget(ID2D1BitmapRenderTarget) (d2d1.h)
description: Creates a new bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target and has the same size, DPI, and pixel format (but not alpha mode) as the current render target.
helpviewer_keywords: ["CreateCompatibleRenderTarget","CreateCompatibleRenderTarget method [Direct2D]","CreateCompatibleRenderTarget method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateCompatibleRenderTarget method","ID2D1RenderTarget.CreateCompatibleRenderTarget","ID2D1RenderTarget.CreateCompatibleRenderTarget(ID2D1BitmapRenderTarget)","ID2D1RenderTarget::CreateCompatibleRenderTarget","ID2D1RenderTarget::CreateCompatibleRenderTarget(ID2D1BitmapRenderTarget)","d2d1/ID2D1RenderTarget::CreateCompatibleRenderTarget","direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_overload1","direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_ptr_ptr_ID2D1BitmapRenderTarget"]
old-location: direct2d\ID2D1RenderTarget_CreateCompatibleRenderTarget_overload1.htm
tech.root: Direct2D
ms.assetid: e36fbf45-9827-4ea0-ac52-676ba826a7d3
ms.date: 12/05/2018
ms.keywords: CreateCompatibleRenderTarget, CreateCompatibleRenderTarget method [Direct2D], CreateCompatibleRenderTarget method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateCompatibleRenderTarget method, ID2D1RenderTarget.CreateCompatibleRenderTarget, ID2D1RenderTarget.CreateCompatibleRenderTarget(ID2D1BitmapRenderTarget), ID2D1RenderTarget::CreateCompatibleRenderTarget, ID2D1RenderTarget::CreateCompatibleRenderTarget(ID2D1BitmapRenderTarget), d2d1/ID2D1RenderTarget::CreateCompatibleRenderTarget, direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_overload1, direct2d.ID2D1RenderTarget_CreateCompatibleRenderTarget_ptr_ptr_ID2D1BitmapRenderTarget
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
 - ID2D1RenderTarget::CreateCompatibleRenderTarget
 - d2d1/ID2D1RenderTarget::CreateCompatibleRenderTarget
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
 - ID2D1RenderTarget.CreateCompatibleRenderTarget
---

## -description

Creates a new bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target and has the same size, DPI, and pixel format (but not alpha mode) as the current render target.

## -parameters

### -param bitmapRenderTarget

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget">ID2D1BitmapRenderTarget</a>**</b>

When this method returns, contains a pointer to a pointer to a new bitmap render target. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

The bitmap render target created by this method is not compatible with GDI, and has an alpha mode of <a href="/windows/win32/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_PREMULTIPLIED</a>.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

