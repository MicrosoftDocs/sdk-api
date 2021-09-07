---
UID: NF:mileffects.IMILBitmapEffectRenderContextImpl.UpdateOutputBounds
title: IMILBitmapEffectRenderContextImpl::UpdateOutputBounds (mileffects.h)
description: Updates the output bounds with the given region.
helpviewer_keywords: ["IMILBitmapEffectRenderContextImpl interface [WPF Bitmap Effects]","UpdateOutputBounds method","IMILBitmapEffectRenderContextImpl.UpdateOutputBounds","IMILBitmapEffectRenderContextImpl::UpdateOutputBounds","UpdateOutputBounds","UpdateOutputBounds method [WPF Bitmap Effects]","UpdateOutputBounds method [WPF Bitmap Effects]","IMILBitmapEffectRenderContextImpl interface","_wibe_imilbitmapeffectrendercontextimpl_updateoutputbounds","mileffects/IMILBitmapEffectRenderContextImpl::UpdateOutputBounds","wibe._wibe_imilbitmapeffectrendercontextimpl_updateoutputbounds"]
old-location: wibe\_wibe_imilbitmapeffectrendercontextimpl_updateoutputbounds.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectrendercontextimpl\updateoutputbounds.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectRenderContextImpl interface [WPF Bitmap Effects],UpdateOutputBounds method, IMILBitmapEffectRenderContextImpl.UpdateOutputBounds, IMILBitmapEffectRenderContextImpl::UpdateOutputBounds, UpdateOutputBounds, UpdateOutputBounds method [WPF Bitmap Effects], UpdateOutputBounds method [WPF Bitmap Effects],IMILBitmapEffectRenderContextImpl interface, _wibe_imilbitmapeffectrendercontextimpl_updateoutputbounds, mileffects/IMILBitmapEffectRenderContextImpl::UpdateOutputBounds, wibe._wibe_imilbitmapeffectrendercontextimpl_updateoutputbounds
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
 - IMILBitmapEffectRenderContextImpl::UpdateOutputBounds
 - mileffects/IMILBitmapEffectRenderContextImpl::UpdateOutputBounds
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
 - IMILBitmapEffectRenderContextImpl.UpdateOutputBounds
---

# IMILBitmapEffectRenderContextImpl::UpdateOutputBounds


## -description

Updates the output bounds with the given region.

## -parameters

### -param pRect [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/ns-mileffects-milrectd">MIL_RECTD</a>*</b>

The new output bounds to use.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.