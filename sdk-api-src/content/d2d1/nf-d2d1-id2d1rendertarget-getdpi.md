---
UID: NF:d2d1.ID2D1RenderTarget.GetDpi
title: ID2D1RenderTarget::GetDpi (d2d1.h)
description: Return the render target's dots per inch (DPI).
helpviewer_keywords: ["GetDpi","GetDpi method [Direct2D]","GetDpi method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","GetDpi method","ID2D1RenderTarget.GetDpi","ID2D1RenderTarget::GetDpi","d2d1/ID2D1RenderTarget::GetDpi","direct2d.ID2D1RenderTarget_GetDpi"]
old-location: direct2d\ID2D1RenderTarget_GetDpi.htm
tech.root: Direct2D
ms.assetid: 72a25b78-96fd-42bf-9e71-6bb80efea0ac
ms.date: 12/05/2018
ms.keywords: GetDpi, GetDpi method [Direct2D], GetDpi method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],GetDpi method, ID2D1RenderTarget.GetDpi, ID2D1RenderTarget::GetDpi, d2d1/ID2D1RenderTarget::GetDpi, direct2d.ID2D1RenderTarget_GetDpi
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
 - ID2D1RenderTarget::GetDpi
 - d2d1/ID2D1RenderTarget::GetDpi
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
 - ID2D1RenderTarget.GetDpi
---

# ID2D1RenderTarget::GetDpi


## -description

Return the render target's dots per inch (DPI).

## -parameters

### -param dpiX [out]

Type: <b>FLOAT*</b>

When this method returns, contains the horizontal DPI of the render target. This parameter is passed uninitialized.

### -param dpiY [out]

Type: <b>FLOAT*</b>

When this method returns, contains the vertical DPI of the render target. This parameter is passed uninitialized.

## -remarks

This method indicates the mapping from pixel space to device-independent space  for the render target.  

For <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>, the DPI defaults to the most recently factory-read system DPI. The default value for all other render targets is 96 DPI.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

