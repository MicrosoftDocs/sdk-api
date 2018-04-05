---
UID: NF:mileffects.IMILBitmapEffectPrimitiveImpl.IsDirty
title: IMILBitmapEffectPrimitiveImpl::IsDirty method
author: windows-driver-content
description: Determines whether the effect needs to be updated.
old-location: wibe\_wibe_imilbitmapeffectprimitiveimpl_isdirty.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitiveimpl\isdirty.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IMILBitmapEffectPrimitiveImpl, IMILBitmapEffectPrimitiveImpl interface [WPF Bitmap Effects], IsDirty method, IMILBitmapEffectPrimitiveImpl::IsDirty, IsDirty method [WPF Bitmap Effects], IsDirty method [WPF Bitmap Effects], IMILBitmapEffectPrimitiveImpl interface, IsDirty,IMILBitmapEffectPrimitiveImpl.IsDirty, _wibe_imilbitmapeffectprimitiveimpl_isdirty, mileffects/IMILBitmapEffectPrimitiveImpl::IsDirty, wibe._wibe_imilbitmapeffectprimitiveimpl_isdirty
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
-	IMILBitmapEffectPrimitiveImpl.IsDirty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectPrimitiveImpl::IsDirty method


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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



