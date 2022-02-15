---
UID: NF:mileffects.IMILBitmapEffectRenderContextImpl.GetTransform
title: IMILBitmapEffectRenderContextImpl::GetTransform (mileffects.h)
description: Gets the matrix transform of the render context.
helpviewer_keywords: ["GetTransform","GetTransform method [WPF Bitmap Effects]","GetTransform method [WPF Bitmap Effects]","IMILBitmapEffectRenderContextImpl interface","IMILBitmapEffectRenderContextImpl interface [WPF Bitmap Effects]","GetTransform method","IMILBitmapEffectRenderContextImpl.GetTransform","IMILBitmapEffectRenderContextImpl::GetTransform","_wibe_imilbitmapeffectrendercontextimpl_gettransform","mileffects/IMILBitmapEffectRenderContextImpl::GetTransform","wibe._wibe_imilbitmapeffectrendercontextimpl_gettransform"]
old-location: wibe\_wibe_imilbitmapeffectrendercontextimpl_gettransform.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontextimpl\gettransform.htm
ms.date: 12/05/2018
ms.keywords: GetTransform, GetTransform method [WPF Bitmap Effects], GetTransform method [WPF Bitmap Effects],IMILBitmapEffectRenderContextImpl interface, IMILBitmapEffectRenderContextImpl interface [WPF Bitmap Effects],GetTransform method, IMILBitmapEffectRenderContextImpl.GetTransform, IMILBitmapEffectRenderContextImpl::GetTransform, _wibe_imilbitmapeffectrendercontextimpl_gettransform, mileffects/IMILBitmapEffectRenderContextImpl::GetTransform, wibe._wibe_imilbitmapeffectrendercontextimpl_gettransform
req.header: mileffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mileffects.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
f1_keywords:
 - IMILBitmapEffectRenderContextImpl::GetTransform
 - mileffects/IMILBitmapEffectRenderContextImpl::GetTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectRenderContextImpl.GetTransform
---

# IMILBitmapEffectRenderContextImpl::GetTransform


## -description

Gets the matrix transform of the render context.

## -parameters

### -param pMatrix [in, out]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/ns-mileffects-milmatrixf">MILMatrixF</a>*</b>

The matrix transform of the render context.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.