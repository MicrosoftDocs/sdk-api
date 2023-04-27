---
UID: NE:wincodec.WICPlanarOptions
title: WICPlanarOptions (wincodec.h)
description: Specifies additional options to an IWICPlanarBitmapSourceTransform implementation.
helpviewer_keywords: ["WICPlanarOptions","WICPlanarOptions enumeration [Windows Imaging Component]","WICPlanarOptionsDefault","WICPlanarOptionsPreserveSubsampling","wic.wicplanaroptions","wincodec/WICPlanarOptions","wincodec/WICPlanarOptionsDefault","wincodec/WICPlanarOptionsPreserveSubsampling"]
old-location: wic\wicplanaroptions.htm
tech.root: wic
ms.assetid: 8B7F34AA-77A0-428D-800E-31AB43067102
ms.date: 12/05/2018
ms.keywords: WICPlanarOptions, WICPlanarOptions enumeration [Windows Imaging Component], WICPlanarOptionsDefault, WICPlanarOptionsPreserveSubsampling, wic.wicplanaroptions, wincodec/WICPlanarOptions, wincodec/WICPlanarOptionsDefault, wincodec/WICPlanarOptionsPreserveSubsampling
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.typenames: WICPlanarOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICPlanarOptions
 - wincodec/WICPlanarOptions
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
 - WICPlanarOptions
---

# WICPlanarOptions enumeration


## -description

Specifies additional options to an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform">IWICPlanarBitmapSourceTransform</a> implementation.

## -enum-fields

### -field WICPlanarOptionsDefault:0

No options specified.  



WIC JPEG Decoder:  The default behavior for iDCT scaling is to preserve quality when downscaling by downscaling only the Y plane in some cases, and the image may change to 4:4:4 chroma subsampling.

### -field WICPlanarOptionsPreserveSubsampling:0x1

Asks the source to preserve the size ratio between planes when scaling.

WIC JPEG Decoder:  Specifying this option causes the JPEG decoder to scale luma and chroma planes by the same amount, so a 4:2:0 chroma subsampled image outputs 4:2:0 data when downscaling by 2x, 4x, or 8x.

### -field WICPLANAROPTIONS_FORCE_DWORD:0x7fffffff

## -see-also

<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels">IWICPlanarBitmapSourceTransform::CopyPixels</a>



<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform">IWICPlanarBitmapSourceTransform::DoesSupportTransform</a>
