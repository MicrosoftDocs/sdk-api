---
UID: NF:wincodec.IWICBitmapSourceTransform.GetClosestPixelFormat
title: IWICBitmapSourceTransform::GetClosestPixelFormat (wincodec.h)
description: Retrieves the closest pixel format to which the implementation of IWICBitmapSourceTransform can natively copy pixels, given a desired format.
helpviewer_keywords: ["GetClosestPixelFormat","GetClosestPixelFormat method [Windows Imaging Component]","GetClosestPixelFormat method [Windows Imaging Component]","IWICBitmapSourceTransform interface","IWICBitmapSourceTransform interface [Windows Imaging Component]","GetClosestPixelFormat method","IWICBitmapSourceTransform.GetClosestPixelFormat","IWICBitmapSourceTransform::GetClosestPixelFormat","_wic_codec_iwicbitmapsourcetransform_getclosestpixelformat","wic._wic_codec_iwicbitmapsourcetransform_getclosestpixelformat","wincodec/IWICBitmapSourceTransform::GetClosestPixelFormat"]
old-location: wic\_wic_codec_iwicbitmapsourcetransform_getclosestpixelformat.htm
tech.root: wic
ms.assetid: 153c5e2a-c42f-4949-9313-48d5e186ecf3
ms.date: 12/05/2018
ms.keywords: GetClosestPixelFormat, GetClosestPixelFormat method [Windows Imaging Component], GetClosestPixelFormat method [Windows Imaging Component],IWICBitmapSourceTransform interface, IWICBitmapSourceTransform interface [Windows Imaging Component],GetClosestPixelFormat method, IWICBitmapSourceTransform.GetClosestPixelFormat, IWICBitmapSourceTransform::GetClosestPixelFormat, _wic_codec_iwicbitmapsourcetransform_getclosestpixelformat, wic._wic_codec_iwicbitmapsourcetransform_getclosestpixelformat, wincodec/IWICBitmapSourceTransform::GetClosestPixelFormat
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
 - IWICBitmapSourceTransform::GetClosestPixelFormat
 - wincodec/IWICBitmapSourceTransform::GetClosestPixelFormat
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
 - IWICBitmapSourceTransform.GetClosestPixelFormat
---

# IWICBitmapSourceTransform::GetClosestPixelFormat


## -description

Retrieves the closest pixel format to which the implementation of <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a> can natively copy pixels, given a desired format.

## -parameters

### -param pguidDstFormat [in, out]

Type: <b>WICPixelFormatGUID*</b>

A pointer that receives the GUID of the pixel format that is the closest supported pixel format of the desired format.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The Windows provided codecs provide the following support:

<ul>
<li>BMP, ICO, GIF, TIFF: No implementation of <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a>.</li>
<li>JPEG, PNG, JPEG-XR: Trivial support (always returns the same value as <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-getpixelformat">IWICBitmapFrameDecode::GetPixelFormat</a>).</li>
</ul>