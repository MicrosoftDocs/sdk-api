---
UID: NF:dwrite.IDWriteBitmapRenderTarget.SetCurrentTransform
title: IDWriteBitmapRenderTarget::SetCurrentTransform (dwrite.h)
description: Sets the transform that maps abstract coordinate to DIPs (device-independent pixel). This does not affect the world transform of the underlying device context.
helpviewer_keywords: ["IDWriteBitmapRenderTarget interface [Direct Write]","SetCurrentTransform method","IDWriteBitmapRenderTarget.SetCurrentTransform","IDWriteBitmapRenderTarget::SetCurrentTransform","SetCurrentTransform","SetCurrentTransform method [Direct Write]","SetCurrentTransform method [Direct Write]","IDWriteBitmapRenderTarget interface","directwrite.IDWriteBitmapRenderTarget_SetCurrentTransform","dwrite/IDWriteBitmapRenderTarget::SetCurrentTransform"]
old-location: directwrite\IDWriteBitmapRenderTarget_SetCurrentTransform.htm
tech.root: DirectWrite
ms.assetid: 970092a4-e5f2-4795-aaf9-e0264a8b1845
ms.date: 12/05/2018
ms.keywords: IDWriteBitmapRenderTarget interface [Direct Write],SetCurrentTransform method, IDWriteBitmapRenderTarget.SetCurrentTransform, IDWriteBitmapRenderTarget::SetCurrentTransform, SetCurrentTransform, SetCurrentTransform method [Direct Write], SetCurrentTransform method [Direct Write],IDWriteBitmapRenderTarget interface, directwrite.IDWriteBitmapRenderTarget_SetCurrentTransform, dwrite/IDWriteBitmapRenderTarget::SetCurrentTransform
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
 - IDWriteBitmapRenderTarget::SetCurrentTransform
 - dwrite/IDWriteBitmapRenderTarget::SetCurrentTransform
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
 - IDWriteBitmapRenderTarget.SetCurrentTransform
---

# IDWriteBitmapRenderTarget::SetCurrentTransform


## -description

 Sets the transform that maps abstract coordinate to DIPs (device-independent pixel). This does not affect the world
     transform of the underlying device context.

## -parameters

### -param transform [in, optional]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a>*</b>

 Specifies the new transform. This parameter can be <b>NULL</b>, in which
     case the identity transform is implied.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget">IDWriteBitmapRenderTarget</a>

