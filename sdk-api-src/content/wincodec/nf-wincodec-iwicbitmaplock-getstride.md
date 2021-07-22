---
UID: NF:wincodec.IWICBitmapLock.GetStride
title: IWICBitmapLock::GetStride (wincodec.h)
description: Provides access to the stride value for the memory.
helpviewer_keywords: ["GetStride","GetStride method [Windows Imaging Component]","GetStride method [Windows Imaging Component]","IWICBitmapLock interface","IWICBitmapLock interface [Windows Imaging Component]","GetStride method","IWICBitmapLock.GetStride","IWICBitmapLock::GetStride","_wic_codec_iwicbitmaplock_getstride","wic._wic_codec_iwicbitmaplock_getstride","wincodec/IWICBitmapLock::GetStride"]
old-location: wic\_wic_codec_iwicbitmaplock_getstride.htm
tech.root: wic
ms.assetid: f4bde79d-29a1-46bf-b7e4-91c39c2f0690
ms.date: 12/05/2018
ms.keywords: GetStride, GetStride method [Windows Imaging Component], GetStride method [Windows Imaging Component],IWICBitmapLock interface, IWICBitmapLock interface [Windows Imaging Component],GetStride method, IWICBitmapLock.GetStride, IWICBitmapLock::GetStride, _wic_codec_iwicbitmaplock_getstride, wic._wic_codec_iwicbitmaplock_getstride, wincodec/IWICBitmapLock::GetStride
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICBitmapLock::GetStride
 - wincodec/IWICBitmapLock::GetStride
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapLock.GetStride
---

# IWICBitmapLock::GetStride


## -description

Provides access to the stride value for the memory.

## -parameters

### -param pcbStride [in, out]

Type: <b>UINT*</b>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Note the stride value is specific to the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmaplock">IWICBitmapLock</a>, not the bitmap. 
            For example, two consecutive locks on the same rectangle of a bitmap may return different pointers and stride values, depending on internal implementation.