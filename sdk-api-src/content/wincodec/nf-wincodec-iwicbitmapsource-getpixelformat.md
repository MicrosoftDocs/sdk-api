---
UID: NF:wincodec.IWICBitmapSource.GetPixelFormat
title: IWICBitmapSource::GetPixelFormat (wincodec.h)
description: Retrieves the pixel format of the bitmap source..
helpviewer_keywords: ["GetPixelFormat","GetPixelFormat method [Windows Imaging Component]","GetPixelFormat method [Windows Imaging Component]","IWICBitmapSource interface","IWICBitmapSource interface [Windows Imaging Component]","GetPixelFormat method","IWICBitmapSource.GetPixelFormat","IWICBitmapSource::GetPixelFormat","_wic_codec_iwicbitmapsource_getpixelformat","wic._wic_codec_iwicbitmapsource_getpixelformat","wincodec/IWICBitmapSource::GetPixelFormat"]
old-location: wic\_wic_codec_iwicbitmapsource_getpixelformat.htm
tech.root: wic
ms.assetid: 6fd30a38-a447-4e4e-93ea-e31c5ba1271e
ms.date: 12/05/2018
ms.keywords: GetPixelFormat, GetPixelFormat method [Windows Imaging Component], GetPixelFormat method [Windows Imaging Component],IWICBitmapSource interface, IWICBitmapSource interface [Windows Imaging Component],GetPixelFormat method, IWICBitmapSource.GetPixelFormat, IWICBitmapSource::GetPixelFormat, _wic_codec_iwicbitmapsource_getpixelformat, wic._wic_codec_iwicbitmapsource_getpixelformat, wincodec/IWICBitmapSource::GetPixelFormat
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
 - IWICBitmapSource::GetPixelFormat
 - wincodec/IWICBitmapSource::GetPixelFormat
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
 - IWICBitmapSource.GetPixelFormat
---

# IWICBitmapSource::GetPixelFormat


## -description

Retrieves the pixel format of the bitmap source..

## -parameters

### -param pPixelFormat [out]

Type: <b>WICPixelFormatGUID*</b>

Receives the pixel format GUID the bitmap is stored in. For a list of available pixel formats, see the <a href="/windows/desktop/wic/-wic-codec-native-pixel-formats">Native Pixel Formats</a> topic.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The pixel format returned by this method is not necessarily the pixel format the image is stored as.
            The codec may perform a format conversion from the storage pixel format to an output pixel format.