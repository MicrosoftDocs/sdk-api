---
UID: NF:mileffects.IMILBitmapEffectImpl.GetInputSourceBounds
title: IMILBitmapEffectImpl::GetInputSourceBounds
author: windows-sdk-content
description: Gets the bounds of the input source.
old-location: wibe\_wibe_imilbitmapeffectimpl_getinputsourcebounds.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\getinputsourcebounds.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInputSourceBounds, GetInputSourceBounds method [WPF Bitmap Effects], GetInputSourceBounds method [WPF Bitmap Effects],IMILBitmapEffectImpl interface, IMILBitmapEffectImpl interface [WPF Bitmap Effects],GetInputSourceBounds method, IMILBitmapEffectImpl.GetInputSourceBounds, IMILBitmapEffectImpl::GetInputSourceBounds, _wibe_imilbitmapeffectimpl_getinputsourcebounds, mileffects/IMILBitmapEffectImpl::GetInputSourceBounds, wibe._wibe_imilbitmapeffectimpl_getinputsourcebounds
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.h
api_name:
 - IMILBitmapEffectImpl.GetInputSourceBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
---

# IMILBitmapEffectImpl::GetInputSourceBounds


## -description


Gets the bounds of the input source.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the bitmap source to retrieve.


### -param pRect [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms735228(v=VS.85).aspx">MIL_RECTD</a>*</b>

Pointer that receives the bounds of the input source.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



