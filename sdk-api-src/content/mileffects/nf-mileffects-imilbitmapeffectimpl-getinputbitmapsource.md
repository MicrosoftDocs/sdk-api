---
UID: NF:mileffects.IMILBitmapEffectImpl.GetInputBitmapSource
title: IMILBitmapEffectImpl::GetInputBitmapSource (mileffects.h)
description: Gets the input bitmap source of the effect of the given render context.
helpviewer_keywords: ["GetInputBitmapSource","GetInputBitmapSource method [WPF Bitmap Effects]","GetInputBitmapSource method [WPF Bitmap Effects]","IMILBitmapEffectImpl interface","IMILBitmapEffectImpl interface [WPF Bitmap Effects]","GetInputBitmapSource method","IMILBitmapEffectImpl.GetInputBitmapSource","IMILBitmapEffectImpl::GetInputBitmapSource","_wibe_imilbitmapeffectimpl_getinputbitmapsource","mileffects/IMILBitmapEffectImpl::GetInputBitmapSource","wibe._wibe_imilbitmapeffectimpl_getinputbitmapsource"]
old-location: wibe\_wibe_imilbitmapeffectimpl_getinputbitmapsource.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\getinputbitmapsource.htm
ms.date: 12/05/2018
ms.keywords: GetInputBitmapSource, GetInputBitmapSource method [WPF Bitmap Effects], GetInputBitmapSource method [WPF Bitmap Effects],IMILBitmapEffectImpl interface, IMILBitmapEffectImpl interface [WPF Bitmap Effects],GetInputBitmapSource method, IMILBitmapEffectImpl.GetInputBitmapSource, IMILBitmapEffectImpl::GetInputBitmapSource, _wibe_imilbitmapeffectimpl_getinputbitmapsource, mileffects/IMILBitmapEffectImpl::GetInputBitmapSource, wibe._wibe_imilbitmapeffectimpl_getinputbitmapsource
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
 - IMILBitmapEffectImpl::GetInputBitmapSource
 - mileffects/IMILBitmapEffectImpl::GetInputBitmapSource
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
 - IMILBitmapEffectImpl.GetInputBitmapSource
---

# IMILBitmapEffectImpl::GetInputBitmapSource


## -description

Gets the input bitmap source of the effect of the given render context.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the of the input bitmap source.

### -param pRenderContext [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectrendercontext">IMILBitmapEffectRenderContext</a>*</b>

A pointer to the <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectrendercontext">IMILBitmapEffectRenderContext</a>.

### -param pfModifyInPlace [in, out]

Type: <b>VARIANT_BOOL*</b>

A value that indicates whether to modify in-place.

### -param ppBitmapSource [out, retval]

Type: <b>IWICBitmapSource**</b>

A pointer that receives a pointer to the input <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource Interface</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.