---
UID: NF:d2d1.ID2D1RenderTarget.GetMaximumBitmapSize
title: ID2D1RenderTarget::GetMaximumBitmapSize (d2d1.h)
description: Gets the maximum size, in device-dependent units (pixels), of any one bitmap dimension supported by the render target.
helpviewer_keywords: ["GetMaximumBitmapSize","GetMaximumBitmapSize method [Direct2D]","GetMaximumBitmapSize method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","GetMaximumBitmapSize method","ID2D1RenderTarget.GetMaximumBitmapSize","ID2D1RenderTarget::GetMaximumBitmapSize","d2d1/ID2D1RenderTarget::GetMaximumBitmapSize","direct2d.id2d1rendertarget_getmaximumbitmapsize"]
old-location: direct2d\id2d1rendertarget_getmaximumbitmapsize.htm
tech.root: Direct2D
ms.assetid: 55953177-4f81-4420-946a-ac03f1669c8f
ms.date: 12/05/2018
ms.keywords: GetMaximumBitmapSize, GetMaximumBitmapSize method [Direct2D], GetMaximumBitmapSize method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],GetMaximumBitmapSize method, ID2D1RenderTarget.GetMaximumBitmapSize, ID2D1RenderTarget::GetMaximumBitmapSize, d2d1/ID2D1RenderTarget::GetMaximumBitmapSize, direct2d.id2d1rendertarget_getmaximumbitmapsize
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
 - ID2D1RenderTarget::GetMaximumBitmapSize
 - d2d1/ID2D1RenderTarget::GetMaximumBitmapSize
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
 - ID2D1RenderTarget.GetMaximumBitmapSize
---

# ID2D1RenderTarget::GetMaximumBitmapSize


## -description

Gets the maximum size, in device-dependent units (pixels), of  any one bitmap dimension supported by the render target.



## -returns

Type: <b>UINT32</b>

 The maximum size, in pixels, of  any one bitmap dimension supported by the render target.

## -remarks

This method returns the maximum texture size of the Direct3D device.

<div class="alert"><b>Note</b>  The software renderer and WARP devices return the value of 16 megapixels (16*1024*1024).  You can create a <a href="/windows/win32/Direct2D/direct2d-portal">Direct2D</a> texture that is this size, but not a Direct3D texture that is this size.</div>
<div> </div>

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

