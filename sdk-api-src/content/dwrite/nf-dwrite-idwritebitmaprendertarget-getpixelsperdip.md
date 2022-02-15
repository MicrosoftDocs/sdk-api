---
UID: NF:dwrite.IDWriteBitmapRenderTarget.GetPixelsPerDip
title: IDWriteBitmapRenderTarget::GetPixelsPerDip (dwrite.h)
description: Gets the number of bitmap pixels per DIP.
helpviewer_keywords: ["GetPixelsPerDip","GetPixelsPerDip method [Direct Write]","GetPixelsPerDip method [Direct Write]","IDWriteBitmapRenderTarget interface","IDWriteBitmapRenderTarget interface [Direct Write]","GetPixelsPerDip method","IDWriteBitmapRenderTarget.GetPixelsPerDip","IDWriteBitmapRenderTarget::GetPixelsPerDip","directwrite.IDWriteBitmapRenderTarget_GetPixelsPerDip","dwrite/IDWriteBitmapRenderTarget::GetPixelsPerDip"]
old-location: directwrite\IDWriteBitmapRenderTarget_GetPixelsPerDip.htm
tech.root: DirectWrite
ms.assetid: 4bf0488d-cc2e-4a95-8d95-f0bd8e5029d6
ms.date: 12/05/2018
ms.keywords: GetPixelsPerDip, GetPixelsPerDip method [Direct Write], GetPixelsPerDip method [Direct Write],IDWriteBitmapRenderTarget interface, IDWriteBitmapRenderTarget interface [Direct Write],GetPixelsPerDip method, IDWriteBitmapRenderTarget.GetPixelsPerDip, IDWriteBitmapRenderTarget::GetPixelsPerDip, directwrite.IDWriteBitmapRenderTarget_GetPixelsPerDip, dwrite/IDWriteBitmapRenderTarget::GetPixelsPerDip
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
 - IDWriteBitmapRenderTarget::GetPixelsPerDip
 - dwrite/IDWriteBitmapRenderTarget::GetPixelsPerDip
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
 - IDWriteBitmapRenderTarget.GetPixelsPerDip
---

# IDWriteBitmapRenderTarget::GetPixelsPerDip


## -description

 Gets the number of bitmap pixels per DIP.



## -returns

Type: <b>FLOAT</b>

The number of bitmap pixels per DIP.

## -remarks

A DIP (device-independent pixel) is 1/96 inch. Therefore, this value is the number
     if pixels per inch divided by 96.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget">IDWriteBitmapRenderTarget</a>

