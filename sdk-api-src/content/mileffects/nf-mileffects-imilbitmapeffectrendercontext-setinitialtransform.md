---
UID: NF:mileffects.IMILBitmapEffectRenderContext.SetInitialTransform
title: IMILBitmapEffectRenderContext::SetInitialTransform (mileffects.h)
description: Gets the initial MILMatrixF transform.
helpviewer_keywords: ["IMILBitmapEffectRenderContext interface [WPF Bitmap Effects]","SetInitialTransform method","IMILBitmapEffectRenderContext.SetInitialTransform","IMILBitmapEffectRenderContext::SetInitialTransform","SetInitialTransform","SetInitialTransform method [WPF Bitmap Effects]","SetInitialTransform method [WPF Bitmap Effects]","IMILBitmapEffectRenderContext interface","_wibe_imilbitmapeffectrendercontext_setinitialtransform","mileffects/IMILBitmapEffectRenderContext::SetInitialTransform","wibe._wibe_imilbitmapeffectrendercontext_setinitialtransform"]
old-location: wibe\_wibe_imilbitmapeffectrendercontext_setinitialtransform.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontext\setinitialtransform.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectRenderContext interface [WPF Bitmap Effects],SetInitialTransform method, IMILBitmapEffectRenderContext.SetInitialTransform, IMILBitmapEffectRenderContext::SetInitialTransform, SetInitialTransform, SetInitialTransform method [WPF Bitmap Effects], SetInitialTransform method [WPF Bitmap Effects],IMILBitmapEffectRenderContext interface, _wibe_imilbitmapeffectrendercontext_setinitialtransform, mileffects/IMILBitmapEffectRenderContext::SetInitialTransform, wibe._wibe_imilbitmapeffectrendercontext_setinitialtransform
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
 - IMILBitmapEffectRenderContext::SetInitialTransform
 - mileffects/IMILBitmapEffectRenderContext::SetInitialTransform
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
 - IMILBitmapEffectRenderContext.SetInitialTransform
---

# IMILBitmapEffectRenderContext::SetInitialTransform


## -description

Gets the initial <a href="/previous-versions/windows/desktop/api/mileffects/ns-mileffects-milmatrixf">MILMatrixF</a> transform.

## -parameters

### -param pMatrix [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/ns-mileffects-milmatrixf">MILMatrixF</a>*</b>

The initial transform.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.