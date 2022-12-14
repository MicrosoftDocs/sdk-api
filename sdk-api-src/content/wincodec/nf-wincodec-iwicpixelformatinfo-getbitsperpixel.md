---
UID: NF:wincodec.IWICPixelFormatInfo.GetBitsPerPixel
title: IWICPixelFormatInfo::GetBitsPerPixel (wincodec.h)
description: Gets the bits per pixel (BPP) of the pixel format.
helpviewer_keywords: ["GetBitsPerPixel","GetBitsPerPixel method [Windows Imaging Component]","GetBitsPerPixel method [Windows Imaging Component]","IWICPixelFormatInfo interface","IWICPixelFormatInfo interface [Windows Imaging Component]","GetBitsPerPixel method","IWICPixelFormatInfo.GetBitsPerPixel","IWICPixelFormatInfo::GetBitsPerPixel","_wic_codec_iwicpixelformatinfo_getbitsperpixel","wic._wic_codec_iwicpixelformatinfo_getbitsperpixel","wincodec/IWICPixelFormatInfo::GetBitsPerPixel"]
old-location: wic\_wic_codec_iwicpixelformatinfo_getbitsperpixel.htm
tech.root: wic
ms.assetid: 484fb014-5999-46b9-8e32-3fd5296e483f
ms.date: 12/05/2018
ms.keywords: GetBitsPerPixel, GetBitsPerPixel method [Windows Imaging Component], GetBitsPerPixel method [Windows Imaging Component],IWICPixelFormatInfo interface, IWICPixelFormatInfo interface [Windows Imaging Component],GetBitsPerPixel method, IWICPixelFormatInfo.GetBitsPerPixel, IWICPixelFormatInfo::GetBitsPerPixel, _wic_codec_iwicpixelformatinfo_getbitsperpixel, wic._wic_codec_iwicpixelformatinfo_getbitsperpixel, wincodec/IWICPixelFormatInfo::GetBitsPerPixel
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICPixelFormatInfo::GetBitsPerPixel
 - wincodec/IWICPixelFormatInfo::GetBitsPerPixel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICPixelFormatInfo.GetBitsPerPixel
---

# IWICPixelFormatInfo::GetBitsPerPixel


## -description

Gets the bits per pixel (BPP) of the pixel format.

## -parameters

### -param puiBitsPerPixel [out]

Type: <b>UINT*</b>

Pointer that receives the BPP of the pixel format.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

