---
UID: NF:dwrite.IDWriteBitmapRenderTarget.GetCurrentTransform
title: IDWriteBitmapRenderTarget::GetCurrentTransform (dwrite.h)
description: Gets the transform that maps abstract coordinates to DIPs. By default this is the identity transform. Note that this is unrelated to the world transform of the underlying device context.
helpviewer_keywords: ["GetCurrentTransform","GetCurrentTransform method [Direct Write]","GetCurrentTransform method [Direct Write]","IDWriteBitmapRenderTarget interface","IDWriteBitmapRenderTarget interface [Direct Write]","GetCurrentTransform method","IDWriteBitmapRenderTarget.GetCurrentTransform","IDWriteBitmapRenderTarget::GetCurrentTransform","directwrite.IDWriteBitmapRenderTarget_GetCurrentTransform","dwrite/IDWriteBitmapRenderTarget::GetCurrentTransform"]
old-location: directwrite\IDWriteBitmapRenderTarget_GetCurrentTransform.htm
tech.root: DirectWrite
ms.assetid: 7f84e38e-f0e8-4cf7-bad0-d41f24ce9499
ms.date: 12/05/2018
ms.keywords: GetCurrentTransform, GetCurrentTransform method [Direct Write], GetCurrentTransform method [Direct Write],IDWriteBitmapRenderTarget interface, IDWriteBitmapRenderTarget interface [Direct Write],GetCurrentTransform method, IDWriteBitmapRenderTarget.GetCurrentTransform, IDWriteBitmapRenderTarget::GetCurrentTransform, directwrite.IDWriteBitmapRenderTarget_GetCurrentTransform, dwrite/IDWriteBitmapRenderTarget::GetCurrentTransform
req.header: dwrite.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteBitmapRenderTarget::GetCurrentTransform
 - dwrite/IDWriteBitmapRenderTarget::GetCurrentTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteBitmapRenderTarget.GetCurrentTransform
---

# IDWriteBitmapRenderTarget::GetCurrentTransform


## -description

 Gets the transform that maps abstract coordinates to DIPs. By default this is the identity 
     transform. Note that this is unrelated to the world transform of the underlying device
     context.

## -parameters

### -param transform [out]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a>*</b>

When this method returns, contains a transform matrix.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget">IDWriteBitmapRenderTarget</a>

