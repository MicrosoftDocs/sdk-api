---
UID: NF:wincodec.IWICImageEncoder.WriteFrameThumbnail
title: IWICImageEncoder::WriteFrameThumbnail (wincodec.h)
author: windows-sdk-content
description: Encodes the image as a thumbnail to the frame given by the IWICBitmapFrameEncode.
old-location: wic\iwicimageencoder_writeframethumbnail.htm
tech.root: wic
ms.assetid: 5A34F900-73F1-4FFC-B251-F22E0EDDB873
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICImageEncoder interface [Windows Imaging Component],WriteFrameThumbnail method, IWICImageEncoder.WriteFrameThumbnail, IWICImageEncoder::WriteFrameThumbnail, WriteFrameThumbnail, WriteFrameThumbnail method [Windows Imaging Component], WriteFrameThumbnail method [Windows Imaging Component],IWICImageEncoder interface, wic.iwicimageencoder_writeframethumbnail, wincodec/IWICImageEncoder::WriteFrameThumbnail
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICImageEncoder.WriteFrameThumbnail
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICImageEncoder::WriteFrameThumbnail


## -description


Encodes the image as a thumbnail to the frame given by the <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a>. 


## -parameters




### -param pImage [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>*</b>

The Direct2D image that will be encoded.


### -param pFrameEncode [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a>*</b>

The frame encoder on which the thumbnail is set.


### -param pImageParameters [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ns-wincodec-wicimageparameters">WICImageParameters</a>*</b>

Additional parameters to control encoding.



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The image passed in must be created on the same device as in <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder">IWICImagingFactory2::CreateImageEncoder</a>. If the <i>pImageParameters</i> are not specified, a set of useful defaults will be assumed, see <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ns-wincodec-wicimageparameters">WICImageParameters</a> for more info.



You must correctly and independently have set up the <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a> before calling this API.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder">IWICImageEncoder</a>
 

 

