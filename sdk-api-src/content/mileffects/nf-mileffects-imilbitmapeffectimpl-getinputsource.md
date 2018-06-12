---
UID: NF:mileffects.IMILBitmapEffectImpl.GetInputSource
title: IMILBitmapEffectImpl::GetInputSource
author: windows-sdk-content
description: Retrieves the input IWICBitmapSource Interface.
old-location: wibe\_wibe_imilbitmapeffectimpl_getinputsource.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\getinputsource.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: GetInputSource, GetInputSource method [WPF Bitmap Effects], GetInputSource method [WPF Bitmap Effects],IMILBitmapEffectImpl interface, IMILBitmapEffectImpl interface [WPF Bitmap Effects],GetInputSource method, IMILBitmapEffectImpl.GetInputSource, IMILBitmapEffectImpl::GetInputSource, _wibe_imilbitmapeffectimpl_getinputsource, mileffects/IMILBitmapEffectImpl::GetInputSource, wibe._wibe_imilbitmapeffectimpl_getinputsource
ms.prod: windows
ms.technology: windows-sdk
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
 - IMILBitmapEffectImpl.GetInputSource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectImpl::GetInputSource


## -description


Retrieves the input <a href="_wic_codec_iwicbitmapsource">IWICBitmapSource Interface</a>.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the input source.


### -param ppBitmapSource [out, retval]

Type: <b>IWICBitmapSource**</b>

A pointer that receives a pointer to the input bitmap source.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



