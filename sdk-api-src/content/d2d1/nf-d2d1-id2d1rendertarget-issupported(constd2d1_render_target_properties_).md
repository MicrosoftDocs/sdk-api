---
UID: NF:d2d1.ID2D1RenderTarget.IsSupported(constD2D1_RENDER_TARGET_PROPERTIES&)
title: ID2D1RenderTarget::IsSupported(const D2D1_RENDER_TARGET_PROPERTIES &) (d2d1.h)
description: Indicates whether the render target supports the specified properties. (overload 1/2)
helpviewer_keywords: ["ID2D1RenderTarget interface [Direct2D]","IsSupported method","ID2D1RenderTarget.IsSupported","ID2D1RenderTarget.IsSupported(const D2D1_RENDER_TARGET_PROPERTIES &)","ID2D1RenderTarget::IsSupported","ID2D1RenderTarget::IsSupported(const D2D1_RENDER_TARGET_PROPERTIES &)","IsSupported","IsSupported method [Direct2D]","IsSupported method [Direct2D]","ID2D1RenderTarget interface","d2d1/ID2D1RenderTarget::IsSupported","direct2d.id2d1rendertarget_issupported"]
old-location: direct2d\id2d1rendertarget_issupported.htm
tech.root: Direct2D
ms.assetid: d9fbc313-fe82-4425-9c9a-79bfacc08019
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],IsSupported method, ID2D1RenderTarget.IsSupported, ID2D1RenderTarget.IsSupported(const D2D1_RENDER_TARGET_PROPERTIES &), ID2D1RenderTarget::IsSupported, ID2D1RenderTarget::IsSupported(const D2D1_RENDER_TARGET_PROPERTIES &), IsSupported, IsSupported method [Direct2D], IsSupported method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::IsSupported, direct2d.id2d1rendertarget_issupported
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
 - ID2D1RenderTarget::IsSupported
 - d2d1/ID2D1RenderTarget::IsSupported
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
 - ID2D1RenderTarget.IsSupported
---

# ID2D1RenderTarget::IsSupported(const D2D1_RENDER_TARGET_PROPERTIES &)


## -description

Indicates whether the render target supports the specified properties.

## -parameters

### -param renderTargetProperties [in]

Type: <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a>*</b>

The render target properties to test.

## -returns

Type: <b>BOOL</b>

<b>TRUE</b> if the specified render target properties are supported by this render target; otherwise, <b>FALSE</b>.

## -remarks

This method does not evaluate the DPI settings specified by the <i>renderTargetProperties</i> parameter.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

