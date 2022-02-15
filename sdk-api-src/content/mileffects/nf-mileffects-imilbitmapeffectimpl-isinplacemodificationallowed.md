---
UID: NF:mileffects.IMILBitmapEffectImpl.IsInPlaceModificationAllowed
title: IMILBitmapEffectImpl::IsInPlaceModificationAllowed (mileffects.h)
description: Determines whether the effect allows in-place modifications.
helpviewer_keywords: ["IMILBitmapEffectImpl interface [WPF Bitmap Effects]","IsInPlaceModificationAllowed method","IMILBitmapEffectImpl.IsInPlaceModificationAllowed","IMILBitmapEffectImpl::IsInPlaceModificationAllowed","IsInPlaceModificationAllowed","IsInPlaceModificationAllowed method [WPF Bitmap Effects]","IsInPlaceModificationAllowed method [WPF Bitmap Effects]","IMILBitmapEffectImpl interface","_wibe_imilbitmapeffectimpl_isinplacemodificationallowed","mileffects/IMILBitmapEffectImpl::IsInPlaceModificationAllowed","wibe._wibe_imilbitmapeffectimpl_isinplacemodificationallowed"]
old-location: wibe\_wibe_imilbitmapeffectimpl_isinplacemodificationallowed.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\isinplacemodificationallowed.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectImpl interface [WPF Bitmap Effects],IsInPlaceModificationAllowed method, IMILBitmapEffectImpl.IsInPlaceModificationAllowed, IMILBitmapEffectImpl::IsInPlaceModificationAllowed, IsInPlaceModificationAllowed, IsInPlaceModificationAllowed method [WPF Bitmap Effects], IsInPlaceModificationAllowed method [WPF Bitmap Effects],IMILBitmapEffectImpl interface, _wibe_imilbitmapeffectimpl_isinplacemodificationallowed, mileffects/IMILBitmapEffectImpl::IsInPlaceModificationAllowed, wibe._wibe_imilbitmapeffectimpl_isinplacemodificationallowed
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
 - IMILBitmapEffectImpl::IsInPlaceModificationAllowed
 - mileffects/IMILBitmapEffectImpl::IsInPlaceModificationAllowed
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
 - IMILBitmapEffectImpl.IsInPlaceModificationAllowed
---

# IMILBitmapEffectImpl::IsInPlaceModificationAllowed


## -description

Determines whether the effect allows in-place modifications.

## -parameters

### -param pOutputConnector [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectoutputconnector">IMILBitmapEffectOutputConnector</a>*</b>

The output connect to check if in-place modifications are allowed.

### -param pfModifyInPlace [out]

Type: <b>VARIANT_BOOL*</b>

A pointer that receives <code>TRUE</code> if in-place modifications are allowed; otherwise, <code>FALSE</code>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.