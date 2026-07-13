---
UID: NN:wincodec.IWICBitmapScaler
title: IWICBitmapScaler (wincodec.h)
description: Represents a resized version of the input bitmap using a resampling or filtering algorithm.
helpviewer_keywords: ["IWICBitmapScaler","IWICBitmapScaler interface [Windows Imaging Component]","IWICBitmapScaler interface [Windows Imaging Component]","described","_wic_codec_iwicbitmapscaler","wic._wic_codec_iwicbitmapscaler","wincodec/IWICBitmapScaler"]
old-location: wic\_wic_codec_iwicbitmapscaler.htm
tech.root: wic
ms.assetid: cc14be9d-d750-40db-a95f-309b392cefe8
ms.date: 12/05/2018
ms.keywords: IWICBitmapScaler, IWICBitmapScaler interface [Windows Imaging Component], IWICBitmapScaler interface [Windows Imaging Component],described, _wic_codec_iwicbitmapscaler, wic._wic_codec_iwicbitmapscaler, wincodec/IWICBitmapScaler
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
 - IWICBitmapScaler
 - wincodec/IWICBitmapScaler
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
 - IWICBitmapScaler
---

# IWICBitmapScaler interface


## -description

Represents a resized version of the input bitmap using a resampling or filtering algorithm.

## -inheritance

The <b>IWICBitmapScaler</b> interface inherits from <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>. <b>IWICBitmapScaler</b> also has these types of members:

## -remarks

Images can be scaled to larger sizes; however, even with sophisticated scaling algorithms, there is only so much information in the image and artifacts tend to worsen the more you scale up.

The scaler will reapply the resampling algorithm every time <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a> is called. 
            If the scaled image is to be animated, the scaled image should be created once and cached in a new bitmap, after which the <b>IWICBitmapScaler</b> may be released. 
            In this way the scaling algorithm - which may be computationally expensive relative to drawing - is performed only once and the result displayed many times.
         

The scaler is optimized to use the minimum amount of memory required to scale the image correctly. 
            The scaler may be used to produce parts of the image incrementally (banding) by calling <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a> with different rectangles representing the output bands of the image. 
            Resampling typically requires overlapping rectangles from the source image and thus may need to request the same pixels from the source bitmap multiple times. 
            Requesting scanlines out-of-order from some image decoders can have a significant performance penalty. 
            Because of this reason, the scaler is optimized to handle consecutive horizontal bands of scanlines (rectangle width equal to the bitmap width). 
            In this case the accumulator from the previous vertically adjacent rectangle is re-used to avoid duplicate scanline requests from the source. 
            This implies that banded output from the scaler may have better performance if the bands are requested sequentially. 
            Of course if the scaler is simply used to produce a single rectangle output, this concern is eliminated because the scaler will internally request scanlines in the correct order.
