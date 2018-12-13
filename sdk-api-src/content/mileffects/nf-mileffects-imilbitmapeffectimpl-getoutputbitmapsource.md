---
UID: NF:mileffects.IMILBitmapEffectImpl.GetOutputBitmapSource
title: IMILBitmapEffectImpl::GetOutputBitmapSource
author: windows-sdk-content
description: Gets the output bitmap source of the effect of the given render context.
old-location: wibe\_wibe_imilbitmapeffectimpl_getoutputbitmapsource.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\getoutputbitmapsource.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetOutputBitmapSource, GetOutputBitmapSource method [WPF Bitmap Effects], GetOutputBitmapSource method [WPF Bitmap Effects],IMILBitmapEffectImpl interface, IMILBitmapEffectImpl interface [WPF Bitmap Effects],GetOutputBitmapSource method, IMILBitmapEffectImpl.GetOutputBitmapSource, IMILBitmapEffectImpl::GetOutputBitmapSource, _wibe_imilbitmapeffectimpl_getoutputbitmapsource, mileffects/IMILBitmapEffectImpl::GetOutputBitmapSource, wibe._wibe_imilbitmapeffectimpl_getoutputbitmapsource
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
 - IMILBitmapEffectImpl.GetOutputBitmapSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
---

# IMILBitmapEffectImpl::GetOutputBitmapSource


## -description


Gets the output bitmap source of the effect of the given render context.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the of the output bitmap source.


### -param pRenderContext [in]

Type: <b><a href="https://msdn.microsoft.com/0c8fbbba-32e6-459c-90ab-2453b57c27ee">IMILBitmapEffectRenderContext</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/0c8fbbba-32e6-459c-90ab-2453b57c27ee">IMILBitmapEffectRenderContext</a>.


### -param pfModifyInPlace [in, out]

Type: <b>VARIANT_BOOL*</b>

A value that indicates whether to modify in-place.


### -param ppBitmapSource [out, retval]

Type: <b>IWICBitmapSource**</b>

A pointer that receives a pointer to the output <a href="_wic_codec_iwicbitmapsource">IWICBitmapSource Interface</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



