---
UID: NF:mileffects.IMILBitmapEffectPrimitive.HasInverseTransform
title: IMILBitmapEffectPrimitive::HasInverseTransform
author: windows-driver-content
description: Determines whether the effect has an inverse transform.
old-location: wibe\_wibe_imilbitmapeffectprimitive_hasinversetransform.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitive\hasinversetransform.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: HasInverseTransform, HasInverseTransform method [WPF Bitmap Effects], HasInverseTransform method [WPF Bitmap Effects],IMILBitmapEffectPrimitive interface, IMILBitmapEffectPrimitive interface [WPF Bitmap Effects],HasInverseTransform method, IMILBitmapEffectPrimitive.HasInverseTransform, IMILBitmapEffectPrimitive::HasInverseTransform, _wibe_imilbitmapeffectprimitive_hasinversetransform, mileffects/IMILBitmapEffectPrimitive::HasInverseTransform, wibe._wibe_imilbitmapeffectprimitive_hasinversetransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.h
api_name:
-	IMILBitmapEffectPrimitive.HasInverseTransform
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectPrimitive::HasInverseTransform


## -description


Determines whether the effect has an inverse transform.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

A zero based index value indicating the output pin through which to query.


### -param pfHasInverse [out]

Type: <b>VARIANT_BOOL*</b>

When this method returns, contains a value indicating whether the effect has an inverse transform.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



