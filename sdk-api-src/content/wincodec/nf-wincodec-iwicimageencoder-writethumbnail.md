---
UID: NF:wincodec.IWICImageEncoder.WriteThumbnail
title: IWICImageEncoder::WriteThumbnail (wincodec.h)
description: Encodes the given image as the thumbnail to the given WIC bitmap encoder.
helpviewer_keywords: ["IWICImageEncoder interface [Windows Imaging Component]","WriteThumbnail method","IWICImageEncoder.WriteThumbnail","IWICImageEncoder::WriteThumbnail","WriteThumbnail","WriteThumbnail method [Windows Imaging Component]","WriteThumbnail method [Windows Imaging Component]","IWICImageEncoder interface","wic.iwicimageencoder_writethumbnail","wincodec/IWICImageEncoder::WriteThumbnail"]
old-location: wic\iwicimageencoder_writethumbnail.htm
tech.root: wic
ms.assetid: 322AD13D-E755-45BD-A31D-D603DBD7FA81
ms.date: 12/05/2018
ms.keywords: IWICImageEncoder interface [Windows Imaging Component],WriteThumbnail method, IWICImageEncoder.WriteThumbnail, IWICImageEncoder::WriteThumbnail, WriteThumbnail, WriteThumbnail method [Windows Imaging Component], WriteThumbnail method [Windows Imaging Component],IWICImageEncoder interface, wic.iwicimageencoder_writethumbnail, wincodec/IWICImageEncoder::WriteThumbnail
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
 - IWICImageEncoder::WriteThumbnail
 - wincodec/IWICImageEncoder::WriteThumbnail
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
 - IWICImageEncoder.WriteThumbnail
---

# IWICImageEncoder::WriteThumbnail


## -description

Encodes the given image as the thumbnail to the given WIC bitmap encoder.

## -parameters

### -param pImage [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>*</b>

The Direct2D image that will be encoded.

### -param pEncoder [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a>*</b>

The encoder on which the thumbnail is set.

### -param pImageParameters [in]

Type: <b>const <a href="/windows/desktop/api/wincodec/ns-wincodec-wicimageparameters">WICImageParameters</a>*</b>

Additional parameters to control encoding.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You must create the image that you pass in on the same device as in <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder">IWICImagingFactory2::CreateImageEncoder</a>. If you don't specify additional parameters in the variable that <i>pImageParameters</i> points to, the encoder uses a set of useful defaults. For info about these defaults, see <a href="/windows/desktop/api/wincodec/ns-wincodec-wicimageparameters">WICImageParameters</a>. 

Before you call <b>WriteThumbnail</b>, you must set up the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a> interface for the encoder on which you want to set the thumbnail. 

If <b>WriteThumbnail</b> fails, it might return E_OUTOFMEMORY, D2DERR_WRONG_RESOURCE_DOMAIN, or other error codes from the encoder.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder">IWICImageEncoder</a>



<a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder">IWICImagingFactory2::CreateImageEncoder</a>



<a href="/windows/desktop/api/wincodec/ns-wincodec-wicimageparameters">WICImageParameters</a>