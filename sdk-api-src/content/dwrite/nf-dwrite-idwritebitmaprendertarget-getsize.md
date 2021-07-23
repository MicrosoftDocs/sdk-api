---
UID: NF:dwrite.IDWriteBitmapRenderTarget.GetSize
title: IDWriteBitmapRenderTarget::GetSize (dwrite.h)
description: Gets the dimensions of the target bitmap.
helpviewer_keywords: ["GetSize","GetSize method [Direct Write]","GetSize method [Direct Write]","IDWriteBitmapRenderTarget interface","IDWriteBitmapRenderTarget interface [Direct Write]","GetSize method","IDWriteBitmapRenderTarget.GetSize","IDWriteBitmapRenderTarget::GetSize","directwrite.IDWriteBitmapRenderTarget_GetSize","dwrite/IDWriteBitmapRenderTarget::GetSize"]
old-location: directwrite\IDWriteBitmapRenderTarget_GetSize.htm
tech.root: DirectWrite
ms.assetid: 1b73854c-674a-408a-8967-e72808ee296e
ms.date: 12/05/2018
ms.keywords: GetSize, GetSize method [Direct Write], GetSize method [Direct Write],IDWriteBitmapRenderTarget interface, IDWriteBitmapRenderTarget interface [Direct Write],GetSize method, IDWriteBitmapRenderTarget.GetSize, IDWriteBitmapRenderTarget::GetSize, directwrite.IDWriteBitmapRenderTarget_GetSize, dwrite/IDWriteBitmapRenderTarget::GetSize
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
 - IDWriteBitmapRenderTarget::GetSize
 - dwrite/IDWriteBitmapRenderTarget::GetSize
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
 - IDWriteBitmapRenderTarget.GetSize
---

# IDWriteBitmapRenderTarget::GetSize


## -description

 Gets the dimensions of the target bitmap.

## -parameters

### -param size [out]

Type: <b>SIZE*</b>

Returns  the width and height of the bitmap in pixels.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget">IDWriteBitmapRenderTarget</a>

