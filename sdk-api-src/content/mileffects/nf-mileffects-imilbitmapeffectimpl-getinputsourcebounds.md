---
UID: NF:mileffects.IMILBitmapEffectImpl.GetInputSourceBounds
title: IMILBitmapEffectImpl::GetInputSourceBounds (mileffects.h)
description: Gets the bounds of the input source.
helpviewer_keywords: ["GetInputSourceBounds","GetInputSourceBounds method [WPF Bitmap Effects]","GetInputSourceBounds method [WPF Bitmap Effects]","IMILBitmapEffectImpl interface","IMILBitmapEffectImpl interface [WPF Bitmap Effects]","GetInputSourceBounds method","IMILBitmapEffectImpl.GetInputSourceBounds","IMILBitmapEffectImpl::GetInputSourceBounds","_wibe_imilbitmapeffectimpl_getinputsourcebounds","mileffects/IMILBitmapEffectImpl::GetInputSourceBounds","wibe._wibe_imilbitmapeffectimpl_getinputsourcebounds"]
old-location: wibe\_wibe_imilbitmapeffectimpl_getinputsourcebounds.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\getinputsourcebounds.htm
ms.date: 12/05/2018
ms.keywords: GetInputSourceBounds, GetInputSourceBounds method [WPF Bitmap Effects], GetInputSourceBounds method [WPF Bitmap Effects],IMILBitmapEffectImpl interface, IMILBitmapEffectImpl interface [WPF Bitmap Effects],GetInputSourceBounds method, IMILBitmapEffectImpl.GetInputSourceBounds, IMILBitmapEffectImpl::GetInputSourceBounds, _wibe_imilbitmapeffectimpl_getinputsourcebounds, mileffects/IMILBitmapEffectImpl::GetInputSourceBounds, wibe._wibe_imilbitmapeffectimpl_getinputsourcebounds
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
f1_keywords:
 - IMILBitmapEffectImpl::GetInputSourceBounds
 - mileffects/IMILBitmapEffectImpl::GetInputSourceBounds
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.h
api_name:
 - IMILBitmapEffectImpl.GetInputSourceBounds
---

# IMILBitmapEffectImpl::GetInputSourceBounds


## -description

Gets the bounds of the input source.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the bitmap source to retrieve.

### -param pRect [out]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/ns-mileffects-milrectd">MIL_RECTD</a>*</b>

Pointer that receives the bounds of the input source.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.