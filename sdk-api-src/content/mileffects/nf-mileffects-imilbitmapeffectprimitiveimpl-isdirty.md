---
UID: NF:mileffects.IMILBitmapEffectPrimitiveImpl.IsDirty
title: IMILBitmapEffectPrimitiveImpl::IsDirty (mileffects.h)
description: Determines whether the effect needs to be updated.
helpviewer_keywords: ["IMILBitmapEffectPrimitiveImpl interface [WPF Bitmap Effects]","IsDirty method","IMILBitmapEffectPrimitiveImpl.IsDirty","IMILBitmapEffectPrimitiveImpl::IsDirty","IsDirty","IsDirty method [WPF Bitmap Effects]","IsDirty method [WPF Bitmap Effects]","IMILBitmapEffectPrimitiveImpl interface","_wibe_imilbitmapeffectprimitiveimpl_isdirty","mileffects/IMILBitmapEffectPrimitiveImpl::IsDirty","wibe._wibe_imilbitmapeffectprimitiveimpl_isdirty"]
old-location: wibe\_wibe_imilbitmapeffectprimitiveimpl_isdirty.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitiveimpl\isdirty.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectPrimitiveImpl interface [WPF Bitmap Effects],IsDirty method, IMILBitmapEffectPrimitiveImpl.IsDirty, IMILBitmapEffectPrimitiveImpl::IsDirty, IsDirty, IsDirty method [WPF Bitmap Effects], IsDirty method [WPF Bitmap Effects],IMILBitmapEffectPrimitiveImpl interface, _wibe_imilbitmapeffectprimitiveimpl_isdirty, mileffects/IMILBitmapEffectPrimitiveImpl::IsDirty, wibe._wibe_imilbitmapeffectprimitiveimpl_isdirty
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
 - IMILBitmapEffectPrimitiveImpl::IsDirty
 - mileffects/IMILBitmapEffectPrimitiveImpl::IsDirty
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
 - IMILBitmapEffectPrimitiveImpl.IsDirty
---

# IMILBitmapEffectPrimitiveImpl::IsDirty


## -description

Determines whether the effect needs to be updated.

## -parameters

### -param uiOutputIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating the output pin to query.

### -param pfDirty [out, retval]

Type: <b>VARIANT_BOOL*</b>

When this method returns, contains a value indicating whether the effect needs to be updated.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

