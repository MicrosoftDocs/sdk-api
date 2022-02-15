---
UID: NF:d2d1.ID2D1RenderTarget.GetTextRenderingParams
title: ID2D1RenderTarget::GetTextRenderingParams (d2d1.h)
description: Retrieves the render target's current text rendering options.
helpviewer_keywords: ["GetTextRenderingParams","GetTextRenderingParams method [Direct2D]","GetTextRenderingParams method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","GetTextRenderingParams method","ID2D1RenderTarget.GetTextRenderingParams","ID2D1RenderTarget::GetTextRenderingParams","d2d1/ID2D1RenderTarget::GetTextRenderingParams","direct2d.ID2D1RenderTarget_GetTextRenderingParams"]
old-location: direct2d\ID2D1RenderTarget_GetTextRenderingParams.htm
tech.root: Direct2D
ms.assetid: 563a13c9-7f13-4b38-afa1-72e847dc8349
ms.date: 12/05/2018
ms.keywords: GetTextRenderingParams, GetTextRenderingParams method [Direct2D], GetTextRenderingParams method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],GetTextRenderingParams method, ID2D1RenderTarget.GetTextRenderingParams, ID2D1RenderTarget::GetTextRenderingParams, d2d1/ID2D1RenderTarget::GetTextRenderingParams, direct2d.ID2D1RenderTarget_GetTextRenderingParams
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
 - ID2D1RenderTarget::GetTextRenderingParams
 - d2d1/ID2D1RenderTarget::GetTextRenderingParams
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
 - ID2D1RenderTarget.GetTextRenderingParams
---

# ID2D1RenderTarget::GetTextRenderingParams


## -description

Retrieves the render target's current text rendering options.

## -parameters

### -param textRenderingParams [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams">IDWriteRenderingParams</a>**</b>

 When this method returns, <i>textRenderingParams</i> contains the address  of a pointer to the render target's current text rendering options.

## -remarks

If the settings specified by  <i>textRenderingParams</i> are incompatible with the render target's text antialiasing mode (specified by <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode">SetTextAntialiasMode</a>), subsequent text and glyph drawing operations will fail and put the render target into an error state.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode">SetTextAntialiasMode</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams">SetTextRenderingParams</a>

