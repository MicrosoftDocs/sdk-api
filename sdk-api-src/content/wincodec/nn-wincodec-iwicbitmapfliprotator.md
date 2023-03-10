---
UID: NN:wincodec.IWICBitmapFlipRotator
title: IWICBitmapFlipRotator (wincodec.h)
description: Exposes methods that produce a flipped (horizontal or vertical) and/or rotated (by 90 degree increments) bitmap source. The flip is done before the rotation.
helpviewer_keywords: ["IWICBitmapFlipRotator","IWICBitmapFlipRotator interface [Windows Imaging Component]","IWICBitmapFlipRotator interface [Windows Imaging Component]","described","_wic_codec_iwicbitmapfliprotator","wic._wic_codec_iwicbitmapfliprotator","wincodec/IWICBitmapFlipRotator"]
old-location: wic\_wic_codec_iwicbitmapfliprotator.htm
tech.root: wic
ms.assetid: 1fcb19ba-34bd-48c0-9964-0c973c31cacc
ms.date: 12/05/2018
ms.keywords: IWICBitmapFlipRotator, IWICBitmapFlipRotator interface [Windows Imaging Component], IWICBitmapFlipRotator interface [Windows Imaging Component],described, _wic_codec_iwicbitmapfliprotator, wic._wic_codec_iwicbitmapfliprotator, wincodec/IWICBitmapFlipRotator
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
 - IWICBitmapFlipRotator
 - wincodec/IWICBitmapFlipRotator
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
 - IWICBitmapFlipRotator
---

# IWICBitmapFlipRotator interface


## -description

Exposes methods that produce a flipped (horizontal or vertical) and/or rotated (by 90 degree increments) bitmap source. The flip is done before the rotation.

## -inheritance

The <b>IWICBitmapFlipRotator</b> interface inherits from <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>. <b>IWICBitmapFlipRotator</b> also has these types of members:

## -remarks

IWICBitmapFipRotator requests data on a per-pixel basis, while WIC codecs provide data on a per-scanline basis. This causes the fliprotator object to exhibit n² behavior if there is no buffering.  This occurs because each pixel in the transformed image requires an entire scanline to be decoded in the file. It is recommended that you buffer the image using <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>, or flip/rotate the image using Direct2D.
