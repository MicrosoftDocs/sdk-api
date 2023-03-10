---
UID: NF:wincodec.IWICImageEncoder.WriteFrame
title: IWICImageEncoder::WriteFrame (wincodec.h)
description: Encodes the image to the frame given by the IWICBitmapFrameEncode.
helpviewer_keywords: ["IWICImageEncoder interface [Windows Imaging Component]","WriteFrame method","IWICImageEncoder.WriteFrame","IWICImageEncoder::WriteFrame","WriteFrame","WriteFrame method [Windows Imaging Component]","WriteFrame method [Windows Imaging Component]","IWICImageEncoder interface","wic.iwicimageencoder_writeframe","wincodec/IWICImageEncoder::WriteFrame"]
old-location: wic\iwicimageencoder_writeframe.htm
tech.root: wic
ms.assetid: 08CD0CE4-5948-4A8F-AA96-9A2BF43EC6D3
ms.date: 12/05/2018
ms.keywords: IWICImageEncoder interface [Windows Imaging Component],WriteFrame method, IWICImageEncoder.WriteFrame, IWICImageEncoder::WriteFrame, WriteFrame, WriteFrame method [Windows Imaging Component], WriteFrame method [Windows Imaging Component],IWICImageEncoder interface, wic.iwicimageencoder_writeframe, wincodec/IWICImageEncoder::WriteFrame
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
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICImageEncoder::WriteFrame
 - wincodec/IWICImageEncoder::WriteFrame
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
 - IWICImageEncoder.WriteFrame
---

# IWICImageEncoder::WriteFrame


## -description

Encodes the image to the frame given by the <a href="/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a>.

## -parameters

### -param pImage [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>*</b>

The Direct2D image that will be encoded.

### -param pFrameEncode [in]

Type: <b><a href="/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a>*</b>

The frame encoder to which the image is written.

### -param pImageParameters [in]

Type: <b>const <a href="/windows/desktop/api/wincodec/ns-wincodec-wicimageparameters">WICImageParameters</a>*</b>

Additional parameters to control encoding.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The image passed in must be created on the same device as in <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder">IWICImagingFactory2::CreateImageEncoder</a>. If the <i>pImageParameters</i> are not specified, a set of useful defaults will be assumed, see <a href="/windows/desktop/api/wincodec/ns-wincodec-wicimageparameters">WICImageParameters</a> for more info.



You must correctly and independently have set up the <a href="/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a> before calling this API.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder">IWICImageEncoder</a>