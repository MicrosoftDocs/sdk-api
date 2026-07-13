---
UID: NF:mileffects.IMILBitmapEffectImpl.GetOutputBitmapSource
title: IMILBitmapEffectImpl::GetOutputBitmapSource (mileffects.h)
description: Gets the output bitmap source of the effect of the given render context.
helpviewer_keywords: ["GetOutputBitmapSource","GetOutputBitmapSource method [WPF Bitmap Effects]","GetOutputBitmapSource method [WPF Bitmap Effects]","IMILBitmapEffectImpl interface","IMILBitmapEffectImpl interface [WPF Bitmap Effects]","GetOutputBitmapSource method","IMILBitmapEffectImpl.GetOutputBitmapSource","IMILBitmapEffectImpl::GetOutputBitmapSource","_wibe_imilbitmapeffectimpl_getoutputbitmapsource","mileffects/IMILBitmapEffectImpl::GetOutputBitmapSource","wibe._wibe_imilbitmapeffectimpl_getoutputbitmapsource"]
old-location: wibe\_wibe_imilbitmapeffectimpl_getoutputbitmapsource.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectimpl\getoutputbitmapsource.htm
ms.date: 12/05/2018
ms.keywords: GetOutputBitmapSource, GetOutputBitmapSource method [WPF Bitmap Effects], GetOutputBitmapSource method [WPF Bitmap Effects],IMILBitmapEffectImpl interface, IMILBitmapEffectImpl interface [WPF Bitmap Effects],GetOutputBitmapSource method, IMILBitmapEffectImpl.GetOutputBitmapSource, IMILBitmapEffectImpl::GetOutputBitmapSource, _wibe_imilbitmapeffectimpl_getoutputbitmapsource, mileffects/IMILBitmapEffectImpl::GetOutputBitmapSource, wibe._wibe_imilbitmapeffectimpl_getoutputbitmapsource
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
 - IMILBitmapEffectImpl::GetOutputBitmapSource
 - mileffects/IMILBitmapEffectImpl::GetOutputBitmapSource
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
 - IMILBitmapEffectImpl.GetOutputBitmapSource
---

# IMILBitmapEffectImpl::GetOutputBitmapSource


## -description

Gets the output bitmap source of the effect of the given render context.

## -parameters

### -param uiIndex [in]

Type: <b>ULONG</b>

The index of the of the output bitmap source.

### -param pRenderContext [in]

Type: <b><a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectrendercontext">IMILBitmapEffectRenderContext</a>*</b>

A pointer to the <a href="/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectrendercontext">IMILBitmapEffectRenderContext</a>.

### -param pfModifyInPlace [in, out]

Type: <b>VARIANT_BOOL*</b>

A value that indicates whether to modify in-place.

### -param ppBitmapSource [out, retval]

Type: <b>IWICBitmapSource**</b>

A pointer that receives a pointer to the output <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource Interface</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.