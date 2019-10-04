---
UID: NF:wincodec.IWICBitmapSourceTransform.GetClosestPixelFormat
title: IWICBitmapSourceTransform::GetClosestPixelFormat (wincodec.h)
author: windows-sdk-content
description: Retrieves the closest pixel format to which the implementation of IWICBitmapSourceTransform can natively copy pixels, given a desired format.
old-location: wic\_wic_codec_iwicbitmapsourcetransform_getclosestpixelformat.htm
tech.root: wic
ms.assetid: 153c5e2a-c42f-4949-9313-48d5e186ecf3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetClosestPixelFormat, GetClosestPixelFormat method [Windows Imaging Component], GetClosestPixelFormat method [Windows Imaging Component],IWICBitmapSourceTransform interface, IWICBitmapSourceTransform interface [Windows Imaging Component],GetClosestPixelFormat method, IWICBitmapSourceTransform.GetClosestPixelFormat, IWICBitmapSourceTransform::GetClosestPixelFormat, _wic_codec_iwicbitmapsourcetransform_getclosestpixelformat, wic._wic_codec_iwicbitmapsourcetransform_getclosestpixelformat, wincodec/IWICBitmapSourceTransform::GetClosestPixelFormat
ms.topic: method
f1_keywords: 
 - "wincodec/IWICBitmapSourceTransform.GetClosestPixelFormat"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapSourceTransform::GetClosestPixelFormat


## -description


Retrieves the closest pixel format to which the implementation of <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a> can natively copy pixels, given a desired format.


## -parameters




### -param pguidDstFormat [in, out]

Type: <b>WICPixelFormatGUID*</b>

A pointer that receives the GUID of the pixel format that is the closest supported pixel format of the desired format.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Windows provided codecs provide the following support:

<ul>
<li>BMP, ICO, GIF, TIFF: No implementation of <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a>.</li>
<li>JPEG, PNG, JPEG-XR: Trivial support (always returns the same value as <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-getpixelformat">IWICBitmapFrameDecode::GetPixelFormat</a>).</li>
</ul>


