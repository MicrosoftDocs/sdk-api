---
UID: NF:wincodec.IWICBitmap.SetResolution
title: IWICBitmap::SetResolution (wincodec.h)
description: Changes the physical resolution of the image.
helpviewer_keywords: ["IWICBitmap interface [Windows Imaging Component]","SetResolution method","IWICBitmap.SetResolution","IWICBitmap::SetResolution","SetResolution","SetResolution method [Windows Imaging Component]","SetResolution method [Windows Imaging Component]","IWICBitmap interface","_wic_codec_iwicbitmap_setresolution","wic._wic_codec_iwicbitmap_setresolution","wincodec/IWICBitmap::SetResolution"]
old-location: wic\_wic_codec_iwicbitmap_setresolution.htm
tech.root: wic
ms.assetid: d8b6c600-0ef0-4fa7-a70f-0299e640c196
ms.date: 12/05/2018
ms.keywords: IWICBitmap interface [Windows Imaging Component],SetResolution method, IWICBitmap.SetResolution, IWICBitmap::SetResolution, SetResolution, SetResolution method [Windows Imaging Component], SetResolution method [Windows Imaging Component],IWICBitmap interface, _wic_codec_iwicbitmap_setresolution, wic._wic_codec_iwicbitmap_setresolution, wincodec/IWICBitmap::SetResolution
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
 - IWICBitmap::SetResolution
 - wincodec/IWICBitmap::SetResolution
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
 - IWICBitmap.SetResolution
---

# IWICBitmap::SetResolution


## -description

Changes the physical resolution of the image.

## -parameters

### -param dpiX [in]

Type: <b>double</b>

The horizontal resolution.

### -param dpiY [in]

Type: <b>double</b>

The vertical resolution.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method has no effect on the actual pixels or samples stored in the bitmap. 
            Instead the interpretation of the sampling rate is modified. 
            This means that a 96 DPI image which is 96 pixels wide is one inch. 
            If the physical resolution is modified to 48 DPI, then the bitmap is considered to be 2 inches wide but has the same number of pixels.  
            If the resolution is less than <b>REAL_EPSILON</b> (1.192092896e-07F) the error code <b>WINCODEC_ERR_INVALIDPARAMETER</b> is returned.

