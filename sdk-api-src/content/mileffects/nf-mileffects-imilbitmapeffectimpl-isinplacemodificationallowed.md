---
UID: NF:mileffects.IMILBitmapEffectImpl.IsInPlaceModificationAllowed
title: IMILBitmapEffectImpl::IsInPlaceModificationAllowed
author: windows-sdk-content
description: Determines whether the effect allows in-place modifications.
old-location: wibe\_wibe_imilbitmapeffectimpl_isinplacemodificationallowed.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\isinplacemodificationallowed.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMILBitmapEffectImpl interface [WPF Bitmap Effects],IsInPlaceModificationAllowed method, IMILBitmapEffectImpl.IsInPlaceModificationAllowed, IMILBitmapEffectImpl::IsInPlaceModificationAllowed, IsInPlaceModificationAllowed, IsInPlaceModificationAllowed method [WPF Bitmap Effects], IsInPlaceModificationAllowed method [WPF Bitmap Effects],IMILBitmapEffectImpl interface, _wibe_imilbitmapeffectimpl_isinplacemodificationallowed, mileffects/IMILBitmapEffectImpl::IsInPlaceModificationAllowed, wibe._wibe_imilbitmapeffectimpl_isinplacemodificationallowed
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mileffects.h
req.include-header: 
req.redist: Microsoft .Net 3.0
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
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.h
api_name:
 - IMILBitmapEffectImpl.IsInPlaceModificationAllowed
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectImpl::IsInPlaceModificationAllowed


## -description


Determines whether the effect allows in-place modifications.


## -parameters




### -param pOutputConnector [in]

Type: <b><a href="https://msdn.microsoft.com/36a2d9da-7a25-4316-acdf-8add4016f18f">IMILBitmapEffectOutputConnector</a>*</b>

The output connect to check if in-place modifications are allowed.


### -param pfModifyInPlace [out]

Type: <b>VARIANT_BOOL*</b>

A pointer that receives <code>TRUE</code> if in-place modifications are allowed; otherwise, <code>FALSE</code>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



