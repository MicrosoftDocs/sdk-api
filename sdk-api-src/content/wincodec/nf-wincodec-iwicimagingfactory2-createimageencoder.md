---
UID: NF:wincodec.IWICImagingFactory2.CreateImageEncoder
title: IWICImagingFactory2::CreateImageEncoder (wincodec.h)
description: Creates a new image encoder object.
helpviewer_keywords: ["CreateImageEncoder","CreateImageEncoder method [Windows Imaging Component]","CreateImageEncoder method [Windows Imaging Component]","IWICImagingFactory2 interface","IWICImagingFactory2 interface [Windows Imaging Component]","CreateImageEncoder method","IWICImagingFactory2.CreateImageEncoder","IWICImagingFactory2::CreateImageEncoder","wic.iwicimagingfactory2_createimageencoder","wincodec/IWICImagingFactory2::CreateImageEncoder"]
old-location: wic\iwicimagingfactory2_createimageencoder.htm
tech.root: wic
ms.assetid: 1F75030F-68B0-4333-B3CF-C4ABD8969448
ms.date: 12/05/2018
ms.keywords: CreateImageEncoder, CreateImageEncoder method [Windows Imaging Component], CreateImageEncoder method [Windows Imaging Component],IWICImagingFactory2 interface, IWICImagingFactory2 interface [Windows Imaging Component],CreateImageEncoder method, IWICImagingFactory2.CreateImageEncoder, IWICImagingFactory2::CreateImageEncoder, wic.iwicimagingfactory2_createimageencoder, wincodec/IWICImagingFactory2::CreateImageEncoder
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
 - IWICImagingFactory2::CreateImageEncoder
 - wincodec/IWICImagingFactory2::CreateImageEncoder
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
 - IWICImagingFactory2.CreateImageEncoder
---

# IWICImagingFactory2::CreateImageEncoder


## -description

Creates a new image encoder object.

## -parameters

### -param pD2DDevice [in]

The <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a> object on which the corresponding image encoder is created.

### -param ppWICImageEncoder [out]

A pointer to a variable that receives a pointer to the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder">IWICImageEncoder</a> interface for the encoder object that you can use to encode <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> images.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You must create images to pass to the image encoder  on the same <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> device that you pass to this method.



You are responsible for setting up the bitmap encoder itself through the existing <a href="/windows/desktop/wic/-wic-imp-iwicbitmapencoder">IWICBitmapEncoder</a> APIs. The <b>IWICBitmapEncoder</b> or the <a href="/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a> object is passed to each of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder">IWICImageEncoder</a> methods: <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimageencoder-writethumbnail">WriteThumbnail</a>, <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimageencoder-writeframe">WriteFrame</a>, and <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimageencoder-writeframethumbnail">WriteFrameThumbnail</a>.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2">IWICImagingFactory2</a>