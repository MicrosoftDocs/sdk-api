---
UID: NF:wincodec.IWICBitmapSource.GetResolution
title: IWICBitmapSource::GetResolution (wincodec.h)
description: Retrieves the sampling rate between pixels and physical world measurements.
helpviewer_keywords: ["GetResolution","GetResolution method [Windows Imaging Component]","GetResolution method [Windows Imaging Component]","IWICBitmapSource interface","IWICBitmapSource interface [Windows Imaging Component]","GetResolution method","IWICBitmapSource.GetResolution","IWICBitmapSource::GetResolution","_wic_codec_iwicbitmapsource_getresolution","wic._wic_codec_iwicbitmapsource_getresolution","wincodec/IWICBitmapSource::GetResolution"]
old-location: wic\_wic_codec_iwicbitmapsource_getresolution.htm
tech.root: wic
ms.assetid: 49241ed1-1036-4f88-9116-4727de883b3e
ms.date: 12/05/2018
ms.keywords: GetResolution, GetResolution method [Windows Imaging Component], GetResolution method [Windows Imaging Component],IWICBitmapSource interface, IWICBitmapSource interface [Windows Imaging Component],GetResolution method, IWICBitmapSource.GetResolution, IWICBitmapSource::GetResolution, _wic_codec_iwicbitmapsource_getresolution, wic._wic_codec_iwicbitmapsource_getresolution, wincodec/IWICBitmapSource::GetResolution
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
 - IWICBitmapSource::GetResolution
 - wincodec/IWICBitmapSource::GetResolution
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
 - IWICBitmapSource.GetResolution
---

# IWICBitmapSource::GetResolution


## -description

Retrieves the sampling rate between pixels and physical world measurements.

## -parameters

### -param pDpiX [out]

Type: <b>double*</b>

A pointer that receives the x-axis dpi resolution.

### -param pDpiY [out]

Type: <b>double*</b>

A pointer that receives the y-axis dpi resolution.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Some formats, such as GIF and ICO, do not have full DPI support.
             For GIF, this method calculates the DPI values from the aspect ratio, using a base DPI of (96.0, 96.0).
            The ICO format does not support DPI at all, and the method always returns (96.0,96.0) for ICO images.
         

Additionally, WIC itself does not transform images based on the DPI values in an image.
            It is up to the caller to transform an image based on the resolution returned.

