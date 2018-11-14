---
UID: NF:dwrite.IDWriteBitmapRenderTarget.GetCurrentTransform
title: IDWriteBitmapRenderTarget::GetCurrentTransform
author: windows-sdk-content
description: Gets the transform that maps abstract coordinates to DIPs. By default this is the identity transform. Note that this is unrelated to the world transform of the underlying device context.
old-location: directwrite\IDWriteBitmapRenderTarget_GetCurrentTransform.htm
tech.root: DirectWrite
ms.assetid: 7f84e38e-f0e8-4cf7-bad0-d41f24ce9499
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetCurrentTransform, GetCurrentTransform method [Direct Write], GetCurrentTransform method [Direct Write],IDWriteBitmapRenderTarget interface, IDWriteBitmapRenderTarget interface [Direct Write],GetCurrentTransform method, IDWriteBitmapRenderTarget.GetCurrentTransform, IDWriteBitmapRenderTarget::GetCurrentTransform, directwrite.IDWriteBitmapRenderTarget_GetCurrentTransform, dwrite/IDWriteBitmapRenderTarget::GetCurrentTransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteBitmapRenderTarget.GetCurrentTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteBitmapRenderTarget.GetCurrentTransform
: 
---

# IDWriteBitmapRenderTarget::GetCurrentTransform


## -description


 Gets the transform that maps abstract coordinates to DIPs. By default this is the identity 
     transform. Note that this is unrelated to the world transform of the underlying device
     context.


## -parameters




### -param transform [out]

Type: <b><a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a>*</b>

When this method returns, contains a transform matrix.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9953a9e9-7772-41a3-9cd9-2340a9dd4b6f">IDWriteBitmapRenderTarget</a>
 

 

