---
UID: NF:mileffects.IMILBitmapEffectRenderContextImpl.UpdateTransform
title: IMILBitmapEffectRenderContextImpl::UpdateTransform (mileffects.h)
description: Updates the output transform with the new matrix.
helpviewer_keywords: ["IMILBitmapEffectRenderContextImpl interface [WPF Bitmap Effects]","UpdateTransform method","IMILBitmapEffectRenderContextImpl.UpdateTransform","IMILBitmapEffectRenderContextImpl::UpdateTransform","UpdateTransform","UpdateTransform method [WPF Bitmap Effects]","UpdateTransform method [WPF Bitmap Effects]","IMILBitmapEffectRenderContextImpl interface","_wibe_imilbitmapeffectrendercontextimpl_updatetransform","mileffects/IMILBitmapEffectRenderContextImpl::UpdateTransform","wibe._wibe_imilbitmapeffectrendercontextimpl_updatetransform"]
old-location: wibe\_wibe_imilbitmapeffectrendercontextimpl_updatetransform.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontextimpl\updatetransform.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectRenderContextImpl interface [WPF Bitmap Effects],UpdateTransform method, IMILBitmapEffectRenderContextImpl.UpdateTransform, IMILBitmapEffectRenderContextImpl::UpdateTransform, UpdateTransform, UpdateTransform method [WPF Bitmap Effects], UpdateTransform method [WPF Bitmap Effects],IMILBitmapEffectRenderContextImpl interface, _wibe_imilbitmapeffectrendercontextimpl_updatetransform, mileffects/IMILBitmapEffectRenderContextImpl::UpdateTransform, wibe._wibe_imilbitmapeffectrendercontextimpl_updatetransform
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
 - IMILBitmapEffectRenderContextImpl::UpdateTransform
 - mileffects/IMILBitmapEffectRenderContextImpl::UpdateTransform
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
 - IMILBitmapEffectRenderContextImpl.UpdateTransform
---

# IMILBitmapEffectRenderContextImpl::UpdateTransform


## -description

Updates the output transform with the new matrix.

## -parameters

### -param pMatrix [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/ns-mileffects-milmatrixf">MILMatrixF</a>*</b>

The new transform to use.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.