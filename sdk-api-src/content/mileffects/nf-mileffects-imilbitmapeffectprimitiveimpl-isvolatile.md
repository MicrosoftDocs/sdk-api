---
UID: NF:mileffects.IMILBitmapEffectPrimitiveImpl.IsVolatile
title: IMILBitmapEffectPrimitiveImpl::IsVolatile (mileffects.h)
description: Determines whether the current effect is considered volatile. If an effect is volatile, the effects framework will not attempt to cache the effect's output.
helpviewer_keywords: ["IMILBitmapEffectPrimitiveImpl interface [WPF Bitmap Effects]","IsVolatile method","IMILBitmapEffectPrimitiveImpl.IsVolatile","IMILBitmapEffectPrimitiveImpl::IsVolatile","IsVolatile","IsVolatile method [WPF Bitmap Effects]","IsVolatile method [WPF Bitmap Effects]","IMILBitmapEffectPrimitiveImpl interface","_wibe_imilbitmapeffectprimitiveimpl_isvolatile","mileffects/IMILBitmapEffectPrimitiveImpl::IsVolatile","wibe._wibe_imilbitmapeffectprimitiveimpl_isvolatile"]
old-location: wibe\_wibe_imilbitmapeffectprimitiveimpl_isvolatile.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitiveimpl\isvolatile.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectPrimitiveImpl interface [WPF Bitmap Effects],IsVolatile method, IMILBitmapEffectPrimitiveImpl.IsVolatile, IMILBitmapEffectPrimitiveImpl::IsVolatile, IsVolatile, IsVolatile method [WPF Bitmap Effects], IsVolatile method [WPF Bitmap Effects],IMILBitmapEffectPrimitiveImpl interface, _wibe_imilbitmapeffectprimitiveimpl_isvolatile, mileffects/IMILBitmapEffectPrimitiveImpl::IsVolatile, wibe._wibe_imilbitmapeffectprimitiveimpl_isvolatile
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
 - IMILBitmapEffectPrimitiveImpl::IsVolatile
 - mileffects/IMILBitmapEffectPrimitiveImpl::IsVolatile
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
 - IMILBitmapEffectPrimitiveImpl.IsVolatile
---

# IMILBitmapEffectPrimitiveImpl::IsVolatile


## -description

Determines whether the current effect is considered volatile. If an effect is volatile, the effects framework will not attempt to cache the effect's output.

## -parameters

### -param uiOutputIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating the output pin to query.

### -param pfVolatile [out, retval]

Type: <b>VARIANT_BOOL*</b>

When this method returns, contains a value indicating whether the effect is considered volatile.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

