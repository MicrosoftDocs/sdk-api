---
UID: NS:wincodec.WICImageParameters
title: WICImageParameters (wincodec.h)
description: This defines parameters that you can use to override the default parameters normally used when encoding an image.
helpviewer_keywords: ["PWICImageParameters","PWICImageParameters structure pointer [Windows Imaging Component]","WICImageParameters","WICImageParameters structure [Windows Imaging Component]","wic.wicimageparameters","wincodec/PWICImageParameters","wincodec/WICImageParameters"]
old-location: wic\wicimageparameters.htm
tech.root: wic
ms.assetid: 0B461697-C7ED-48C9-A880-1B5F4A26FCFC
ms.date: 12/05/2018
ms.keywords: PWICImageParameters, PWICImageParameters structure pointer [Windows Imaging Component], WICImageParameters, WICImageParameters structure [Windows Imaging Component], wic.wicimageparameters, wincodec/PWICImageParameters, wincodec/WICImageParameters
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: WICImageParameters
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICImageParameters
 - wincodec/WICImageParameters
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
 - WICImageParameters
---

# WICImageParameters structure


## -description

This defines parameters that you can use to override the default parameters normally used when encoding an image.

## -struct-fields

### -field PixelFormat

The pixel format to which the image is processed before it is written to the encoder.

### -field DpiX

The DPI in the x dimension.

### -field DpiY

The DPI in the y dimension.

### -field Top

The top corner in pixels of the image space to be encoded to the destination.

### -field Left

The left corner in pixels of the image space to be encoded to the destination.

### -field PixelWidth

The width in pixels of the part of the image to write.

### -field PixelHeight

The height in pixels of the part of the image to write.

## -remarks

If this parameter is not passed to the encoding API, the encoder uses these settings.

<ul>
<li>A pixel format of (<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM</a>, <a href="/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_PREMULTIPLIED</a>).</li>
<li>An x and y DPI of 96.</li>
<li>The entire image bounds will be used for encoding.</li>
</ul>
<div class="alert"><b>Note</b>  The parameters as specified can't result in a scale. The encoder can use a larger portion of the input image based on the passed in DPI and the pixel width and height.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder">IWICImageEncoder</a>