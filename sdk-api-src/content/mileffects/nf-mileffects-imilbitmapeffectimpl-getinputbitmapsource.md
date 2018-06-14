---
UID: NF:mileffects.IMILBitmapEffectImpl.GetInputBitmapSource
title: IMILBitmapEffectImpl::GetInputBitmapSource
author: windows-sdk-content
description: Gets the input bitmap source of the effect of the given render context.
old-location: wibe\_wibe_imilbitmapeffectimpl_getinputbitmapsource.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\getinputbitmapsource.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: GetInputBitmapSource, GetInputBitmapSource method [WPF Bitmap Effects], GetInputBitmapSource method [WPF Bitmap Effects],IMILBitmapEffectImpl interface, IMILBitmapEffectImpl interface [WPF Bitmap Effects],GetInputBitmapSource method, IMILBitmapEffectImpl.GetInputBitmapSource, IMILBitmapEffectImpl::GetInputBitmapSource, _wibe_imilbitmapeffectimpl_getinputbitmapsource, mileffects/IMILBitmapEffectImpl::GetInputBitmapSource, wibe._wibe_imilbitmapeffectimpl_getinputbitmapsource
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
 - IMILBitmapEffectImpl.GetInputBitmapSource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectImpl::GetInputBitmapSource


## -description


Gets the input bitmap source of the effect of the given render context.


## -parameters




### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the of the input bitmap source.


### -param pRenderContext [in]

Type: <b><a href="https://msdn.microsoft.com/0c8fbbba-32e6-459c-90ab-2453b57c27ee">IMILBitmapEffectRenderContext</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/0c8fbbba-32e6-459c-90ab-2453b57c27ee">IMILBitmapEffectRenderContext</a>.


### -param pfModifyInPlace [in, out]

Type: <b>VARIANT_BOOL*</b>

A value that indicates whether to modify in-place.


### -param ppBitmapSource [out, retval]

Type: <b>IWICBitmapSource**</b>

A pointer that receives a pointer to the input <a href="_wic_codec_iwicbitmapsource">IWICBitmapSource Interface</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



