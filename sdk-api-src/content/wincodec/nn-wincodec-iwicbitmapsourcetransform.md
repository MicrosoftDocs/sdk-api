---
UID: NN:wincodec.IWICBitmapSourceTransform
title: IWICBitmapSourceTransform (wincodec.h)
description: Exposes methods for offloading certain operations to the underlying IWICBitmapSource implementation.
helpviewer_keywords: ["IWICBitmapSourceTransform","IWICBitmapSourceTransform interface [Windows Imaging Component]","IWICBitmapSourceTransform interface [Windows Imaging Component]","described","_wic_codec_iwicbitmapsourcetransform","wic._wic_codec_iwicbitmapsourcetransform","wincodec/IWICBitmapSourceTransform"]
old-location: wic\_wic_codec_iwicbitmapsourcetransform.htm
tech.root: wic
ms.assetid: f9cc348f-d4f0-4e77-90d6-9ff563a1799c
ms.date: 12/05/2018
ms.keywords: IWICBitmapSourceTransform, IWICBitmapSourceTransform interface [Windows Imaging Component], IWICBitmapSourceTransform interface [Windows Imaging Component],described, _wic_codec_iwicbitmapsourcetransform, wic._wic_codec_iwicbitmapsourcetransform, wincodec/IWICBitmapSourceTransform
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
 - IWICBitmapSourceTransform
 - wincodec/IWICBitmapSourceTransform
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
 - IWICBitmapSourceTransform
---

# IWICBitmapSourceTransform interface


## -description

Exposes methods for offloading certain operations to the underlying <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> implementation.

## -inheritance

The <b>IWICBitmapSourceTransform</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICBitmapSourceTransform</b> also has these types of members:

## -remarks

The <b>IWICBitmapSourceTransform</b> interface is implemented by codecs which can natively scale, flip, rotate, or format convert pixels during decoding. As the transformation is combined with the decoding process, native transformation will generally offer performance advantages over non-native transformations. The inbox <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler">IWICBitmapScaler</a>, <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapfliprotator">IWICBitmapFlipRotator</a>, and <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter">IWICFormatConverter</a> implementations all make use of the <a href="/windows/desktop/wic/-wic-imp-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a> interface when they are placed immediately after a supported <a href="/windows/desktop/wic/-wic-imp-iwicbitmapframedecode">IWICBitmapFrameDecode</a>, so in the typical case an application will automatically receive this performance increase and does not need to directly use this interface. However, when chaining multiple transformations, or when implementing a custom transformation, there may be a performance advantage to using the IWICBitmapSourceTransform interface directly.
