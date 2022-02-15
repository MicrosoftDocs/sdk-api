---
UID: NE:wincodec.WICBitmapInterpolationMode
title: WICBitmapInterpolationMode (wincodec.h)
description: Specifies the sampling or filtering mode to use when scaling an image.
helpviewer_keywords: ["WICBitmapInterpolationMode","WICBitmapInterpolationMode enumeration [Windows Imaging Component]","WICBitmapInterpolationModeCubic","WICBitmapInterpolationModeFant","WICBitmapInterpolationModeHighQualityCubic","WICBitmapInterpolationModeLinear","WICBitmapInterpolationModeNearestNeighbor","_wic_codec_wicbitmapinterpolationmode","wic._wic_codec_wicbitmapinterpolationmode","wincodec/WICBitmapInterpolationMode","wincodec/WICBitmapInterpolationModeCubic","wincodec/WICBitmapInterpolationModeFant","wincodec/WICBitmapInterpolationModeHighQualityCubic","wincodec/WICBitmapInterpolationModeLinear","wincodec/WICBitmapInterpolationModeNearestNeighbor"]
old-location: wic\_wic_codec_wicbitmapinterpolationmode.htm
tech.root: wic
ms.assetid: 7c707ab7-7cd5-418f-921c-e9114da92f2a
ms.date: 12/05/2018
ms.keywords: WICBitmapInterpolationMode, WICBitmapInterpolationMode enumeration [Windows Imaging Component], WICBitmapInterpolationModeCubic, WICBitmapInterpolationModeFant, WICBitmapInterpolationModeHighQualityCubic, WICBitmapInterpolationModeLinear, WICBitmapInterpolationModeNearestNeighbor, _wic_codec_wicbitmapinterpolationmode, wic._wic_codec_wicbitmapinterpolationmode, wincodec/WICBitmapInterpolationMode, wincodec/WICBitmapInterpolationModeCubic, wincodec/WICBitmapInterpolationModeFant, wincodec/WICBitmapInterpolationModeHighQualityCubic, wincodec/WICBitmapInterpolationModeLinear, wincodec/WICBitmapInterpolationModeNearestNeighbor
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WICBitmapInterpolationMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICBitmapInterpolationMode
 - wincodec/WICBitmapInterpolationMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodec.h
api_name:
 - WICBitmapInterpolationMode
---

# WICBitmapInterpolationMode enumeration


## -description

Specifies the sampling or filtering mode to use when scaling an image.

## -enum-fields

### -field WICBitmapInterpolationModeNearestNeighbor:0

A nearest neighbor interpolation algorithm. Also known as nearest pixel or point interpolation.
            

The output pixel is assigned the value of the pixel that the point falls within. No other pixels are considered.

### -field WICBitmapInterpolationModeLinear:0x1

A bilinear interpolation algorithm.
            

The output pixel values are computed as a weighted average of the nearest four pixels in a 2x2 grid.

### -field WICBitmapInterpolationModeCubic:0x2

A bicubic interpolation algorithm.
            

Destination pixel values are computed as a weighted average of the nearest sixteen pixels in a 4x4 grid.

### -field WICBitmapInterpolationModeFant:0x3

A Fant resampling algorithm.
            

Destination pixel values are computed as a weighted average of the all the pixels that map to the new pixel.

### -field WICBitmapInterpolationModeHighQualityCubic:0x4

A high quality bicubic interpolation algorithm. Destination pixel values are computed using a much denser sampling 
      kernel than regular cubic. The kernel is resized in response to the scale factor, making it suitable for downscaling by factors greater than 2.

<div class="alert"><b>Note</b>  This value is supported beginning with Windows 10.</div>
<div> </div>

### -field WICBITMAPINTERPOLATIONMODE_FORCE_DWORD:0x7fffffff

