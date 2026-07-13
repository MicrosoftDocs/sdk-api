---
UID: NF:mileffects.IMILBitmapEffectPrimitive.HasAffineTransform
title: IMILBitmapEffectPrimitive::HasAffineTransform (mileffects.h)
description: Determines whether the effect has an affine transform.
helpviewer_keywords: ["HasAffineTransform","HasAffineTransform method [WPF Bitmap Effects]","HasAffineTransform method [WPF Bitmap Effects]","IMILBitmapEffectPrimitive interface","IMILBitmapEffectPrimitive interface [WPF Bitmap Effects]","HasAffineTransform method","IMILBitmapEffectPrimitive.HasAffineTransform","IMILBitmapEffectPrimitive::HasAffineTransform","_wibe_imilbitmapeffectprimitive_hasaffinetransform","mileffects/IMILBitmapEffectPrimitive::HasAffineTransform","wibe._wibe_imilbitmapeffectprimitive_hasaffinetransform"]
old-location: wibe\_wibe_imilbitmapeffectprimitive_hasaffinetransform.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitive\hasaffinetransform.htm
ms.date: 12/05/2018
ms.keywords: HasAffineTransform, HasAffineTransform method [WPF Bitmap Effects], HasAffineTransform method [WPF Bitmap Effects],IMILBitmapEffectPrimitive interface, IMILBitmapEffectPrimitive interface [WPF Bitmap Effects],HasAffineTransform method, IMILBitmapEffectPrimitive.HasAffineTransform, IMILBitmapEffectPrimitive::HasAffineTransform, _wibe_imilbitmapeffectprimitive_hasaffinetransform, mileffects/IMILBitmapEffectPrimitive::HasAffineTransform, wibe._wibe_imilbitmapeffectprimitive_hasaffinetransform
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
 - IMILBitmapEffectPrimitive::HasAffineTransform
 - mileffects/IMILBitmapEffectPrimitive::HasAffineTransform
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
 - IMILBitmapEffectPrimitive.HasAffineTransform
---

# IMILBitmapEffectPrimitive::HasAffineTransform


## -description

Determines whether the effect has an affine transform.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating the output pin through which to query.

### -param pfAffine [out]

Type: <b>VARIANT_BOOL*</b>

When this method returns, contains a value indicating whether the effect has an affine transform.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

