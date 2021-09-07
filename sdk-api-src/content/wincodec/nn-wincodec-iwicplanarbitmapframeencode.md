---
UID: NN:wincodec.IWICPlanarBitmapFrameEncode
title: IWICPlanarBitmapFrameEncode (wincodec.h)
description: Allows planar component image pixels to be written to an encoder.
helpviewer_keywords: ["IWICPlanarBitmapFrameEncode","IWICPlanarBitmapFrameEncode interface [Windows Imaging Component]","IWICPlanarBitmapFrameEncode interface [Windows Imaging Component]","described","wic.iwicplanarbitmapframeencode","wincodec/IWICPlanarBitmapFrameEncode"]
old-location: wic\iwicplanarbitmapframeencode.htm
tech.root: wic
ms.assetid: 7ACA58CC-E132-4836-B955-322375ADDAA1
ms.date: 12/05/2018
ms.keywords: IWICPlanarBitmapFrameEncode, IWICPlanarBitmapFrameEncode interface [Windows Imaging Component], IWICPlanarBitmapFrameEncode interface [Windows Imaging Component],described, wic.iwicplanarbitmapframeencode, wincodec/IWICPlanarBitmapFrameEncode
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
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICPlanarBitmapFrameEncode
 - wincodec/IWICPlanarBitmapFrameEncode
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
 - IWICPlanarBitmapFrameEncode
---

# IWICPlanarBitmapFrameEncode interface


## -description

Allows planar component image pixels to be written to an encoder.   When supported by the encoder, this allows an application to encode planar component image data without first converting to an interleaved pixel format.

You can use

QueryInterface to obtain this interface from the Windows provided implementation of <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a> for the JPEG encoder.

## -inheritance

The <b>IWICPlanarBitmapFrameEncode</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICPlanarBitmapFrameEncode</b> also has these types of members:

## -remarks

Encoding YCbCr data using <b>IWICPlanarBitmapFrameEncode</b> is similar but not identical to encoding interleaved data using <a href="/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a>. The planar interface only exposes the ability to write planar frame image data, and you should continue to use the frame encode interface to set metadata or a thumbnail and to commit at the end of the operation.

## -see-also

<a href="/windows/desktop/wic/jpeg-ycbcr-support">JPEG YCbCr Support</a>
