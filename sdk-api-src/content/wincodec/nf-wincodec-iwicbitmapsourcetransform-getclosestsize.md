---
UID: NF:wincodec.IWICBitmapSourceTransform.GetClosestSize
title: IWICBitmapSourceTransform::GetClosestSize (wincodec.h)
description: Returns the closest dimensions the implementation can natively scale to given the desired dimensions.
helpviewer_keywords: ["GetClosestSize","GetClosestSize method [Windows Imaging Component]","GetClosestSize method [Windows Imaging Component]","IWICBitmapSourceTransform interface","IWICBitmapSourceTransform interface [Windows Imaging Component]","GetClosestSize method","IWICBitmapSourceTransform.GetClosestSize","IWICBitmapSourceTransform::GetClosestSize","_wic_codec_iwicbitmapsourcetransform_getclosestsize","wic._wic_codec_iwicbitmapsourcetransform_getclosestsize","wincodec/IWICBitmapSourceTransform::GetClosestSize"]
old-location: wic\_wic_codec_iwicbitmapsourcetransform_getclosestsize.htm
tech.root: wic
ms.assetid: 0eae79dc-d636-4449-ba90-0f296b71573a
ms.date: 12/05/2018
ms.keywords: GetClosestSize, GetClosestSize method [Windows Imaging Component], GetClosestSize method [Windows Imaging Component],IWICBitmapSourceTransform interface, IWICBitmapSourceTransform interface [Windows Imaging Component],GetClosestSize method, IWICBitmapSourceTransform.GetClosestSize, IWICBitmapSourceTransform::GetClosestSize, _wic_codec_iwicbitmapsourcetransform_getclosestsize, wic._wic_codec_iwicbitmapsourcetransform_getclosestsize, wincodec/IWICBitmapSourceTransform::GetClosestSize
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
 - IWICBitmapSourceTransform::GetClosestSize
 - wincodec/IWICBitmapSourceTransform::GetClosestSize
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
 - IWICBitmapSourceTransform.GetClosestSize
---

# IWICBitmapSourceTransform::GetClosestSize


## -description

Returns the closest dimensions the implementation can natively scale to given the desired dimensions.

## -parameters

### -param puiWidth [in, out]

Type: <b>UINT*</b>

The desired width. A pointer that receives the closest supported width.

### -param puiHeight [in, out]

Type: <b>UINT*</b>

The desired height. A pointer that receives the closest supported height.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The Windows provided codecs provide the following support for native scaling:


<ul>
<li>BMP, ICO, GIF, TIFF: No implementation of <a href="/windows/desktop/wic/-wic-imp-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a>.</li>
<li>PNG: No scaling support.</li>
<li>JPEG: Native down-scaling by a factor of 8, 4, or 2.</li>
<li>JPEG-XR:  Native scaling of the original image by powers of 2.
</li>
</ul>