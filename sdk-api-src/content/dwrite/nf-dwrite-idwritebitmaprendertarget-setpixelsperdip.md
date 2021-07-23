---
UID: NF:dwrite.IDWriteBitmapRenderTarget.SetPixelsPerDip
title: IDWriteBitmapRenderTarget::SetPixelsPerDip (dwrite.h)
description: Sets the number of bitmap pixels per DIP (device-independent pixel). A DIP is 1/96 inch, so this value is the number if pixels per inch divided by 96.
helpviewer_keywords: ["IDWriteBitmapRenderTarget interface [Direct Write]","SetPixelsPerDip method","IDWriteBitmapRenderTarget.SetPixelsPerDip","IDWriteBitmapRenderTarget::SetPixelsPerDip","SetPixelsPerDip","SetPixelsPerDip method [Direct Write]","SetPixelsPerDip method [Direct Write]","IDWriteBitmapRenderTarget interface","directwrite.IDWriteBitmapRenderTarget_SetPixelsPerDip","dwrite/IDWriteBitmapRenderTarget::SetPixelsPerDip"]
old-location: directwrite\IDWriteBitmapRenderTarget_SetPixelsPerDip.htm
tech.root: DirectWrite
ms.assetid: da582190-4a6d-451a-9d42-831e8786570f
ms.date: 12/05/2018
ms.keywords: IDWriteBitmapRenderTarget interface [Direct Write],SetPixelsPerDip method, IDWriteBitmapRenderTarget.SetPixelsPerDip, IDWriteBitmapRenderTarget::SetPixelsPerDip, SetPixelsPerDip, SetPixelsPerDip method [Direct Write], SetPixelsPerDip method [Direct Write],IDWriteBitmapRenderTarget interface, directwrite.IDWriteBitmapRenderTarget_SetPixelsPerDip, dwrite/IDWriteBitmapRenderTarget::SetPixelsPerDip
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
 - IDWriteBitmapRenderTarget::SetPixelsPerDip
 - dwrite/IDWriteBitmapRenderTarget::SetPixelsPerDip
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
 - IDWriteBitmapRenderTarget.SetPixelsPerDip
---

# IDWriteBitmapRenderTarget::SetPixelsPerDip


## -description

 Sets the number of bitmap pixels per DIP (device-independent pixel). A DIP is 1/96 inch, so this value is the number
     if pixels per inch divided by 96.

## -parameters

### -param pixelsPerDip

Type: <b>FLOAT</b>

A value that specifies the number of pixels per DIP.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget">IDWriteBitmapRenderTarget</a>

