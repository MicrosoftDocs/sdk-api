---
UID: NF:wincodec.IWICImageEncoder.WriteFrame
title: IWICImageEncoder::WriteFrame (wincodec.h)
author: windows-sdk-content
description: Encodes the image to the frame given by the IWICBitmapFrameEncode.
old-location: wic\iwicimageencoder_writeframe.htm
tech.root: wic
ms.assetid: 08CD0CE4-5948-4A8F-AA96-9A2BF43EC6D3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICImageEncoder interface [Windows Imaging Component],WriteFrame method, IWICImageEncoder.WriteFrame, IWICImageEncoder::WriteFrame, WriteFrame, WriteFrame method [Windows Imaging Component], WriteFrame method [Windows Imaging Component],IWICImageEncoder interface, wic.iwicimageencoder_writeframe, wincodec/IWICImageEncoder::WriteFrame
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
 - IWICImageEncoder.WriteFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICImageEncoder::WriteFrame


## -description


Encodes the image to the frame given by the <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a>.


## -parameters




### -param pImage [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>*</b>

The Direct2D image that will be encoded.


### -param pFrameEncode [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a>*</b>

The frame encoder to which the image is written.


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
 

 

