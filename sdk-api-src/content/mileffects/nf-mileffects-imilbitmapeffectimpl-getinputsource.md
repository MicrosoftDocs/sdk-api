---
UID: NF:mileffects.IMILBitmapEffectImpl.GetInputSource
title: IMILBitmapEffectImpl::GetInputSource (mileffects.h)
description: Retrieves the input IWICBitmapSource Interface.
helpviewer_keywords: ["GetInputSource","GetInputSource method [WPF Bitmap Effects]","GetInputSource method [WPF Bitmap Effects]","IMILBitmapEffectImpl interface","IMILBitmapEffectImpl interface [WPF Bitmap Effects]","GetInputSource method","IMILBitmapEffectImpl.GetInputSource","IMILBitmapEffectImpl::GetInputSource","_wibe_imilbitmapeffectimpl_getinputsource","mileffects/IMILBitmapEffectImpl::GetInputSource","wibe._wibe_imilbitmapeffectimpl_getinputsource"]
old-location: wibe\_wibe_imilbitmapeffectimpl_getinputsource.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\getinputsource.htm
ms.date: 12/05/2018
ms.keywords: GetInputSource, GetInputSource method [WPF Bitmap Effects], GetInputSource method [WPF Bitmap Effects],IMILBitmapEffectImpl interface, IMILBitmapEffectImpl interface [WPF Bitmap Effects],GetInputSource method, IMILBitmapEffectImpl.GetInputSource, IMILBitmapEffectImpl::GetInputSource, _wibe_imilbitmapeffectimpl_getinputsource, mileffects/IMILBitmapEffectImpl::GetInputSource, wibe._wibe_imilbitmapeffectimpl_getinputsource
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
 - IMILBitmapEffectImpl::GetInputSource
 - mileffects/IMILBitmapEffectImpl::GetInputSource
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
 - IMILBitmapEffectImpl.GetInputSource
---

# IMILBitmapEffectImpl::GetInputSource


## -description

Retrieves the input <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource Interface</a>.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the input source.

### -param ppBitmapSource [out, retval]

Type: <b>IWICBitmapSource**</b>

A pointer that receives a pointer to the input bitmap source.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.