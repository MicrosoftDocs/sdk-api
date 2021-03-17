---
UID: NF:d2d1.ID2D1RenderTarget.SetAntialiasMode
title: ID2D1RenderTarget::SetAntialiasMode (d2d1.h)
description: Sets the antialiasing mode of the render target. The antialiasing mode applies to all subsequent drawing operations, excluding text and glyph drawing operations.
helpviewer_keywords: ["ID2D1RenderTarget interface [Direct2D]","SetAntialiasMode method","ID2D1RenderTarget.SetAntialiasMode","ID2D1RenderTarget::SetAntialiasMode","SetAntialiasMode","SetAntialiasMode method [Direct2D]","SetAntialiasMode method [Direct2D]","ID2D1RenderTarget interface","d2d1/ID2D1RenderTarget::SetAntialiasMode","direct2d.ID2D1RenderTarget_SetAntialiasMode"]
old-location: direct2d\ID2D1RenderTarget_SetAntialiasMode.htm
tech.root: Direct2D
ms.assetid: cd727271-1725-48e1-be39-680b363db2ae
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],SetAntialiasMode method, ID2D1RenderTarget.SetAntialiasMode, ID2D1RenderTarget::SetAntialiasMode, SetAntialiasMode, SetAntialiasMode method [Direct2D], SetAntialiasMode method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::SetAntialiasMode, direct2d.ID2D1RenderTarget_SetAntialiasMode
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
 - ID2D1RenderTarget::SetAntialiasMode
 - d2d1/ID2D1RenderTarget::SetAntialiasMode
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
 - ID2D1RenderTarget.SetAntialiasMode
---

# ID2D1RenderTarget::SetAntialiasMode


## -description

Sets the antialiasing mode of the render target. The antialiasing mode applies to all subsequent drawing operations, excluding text and glyph drawing operations.

## -parameters

### -param antialiasMode

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_antialias_mode">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode for future drawing operations.

## -remarks

To specify the antialiasing mode for text and glyph operations, use the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode">SetTextAntialiasMode</a> method.

## -see-also

<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-getantialiasmode">GetAntialiasMode</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextantialiasmode">SetTextAntialiasMode</a>

