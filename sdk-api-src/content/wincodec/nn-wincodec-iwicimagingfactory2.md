---
UID: NN:wincodec.IWICImagingFactory2
title: IWICImagingFactory2 (wincodec.h)
description: An extension of the WIC factory interface that includes the ability to create an IWICImageEncoder.
helpviewer_keywords: ["IWICImagingFactory2","IWICImagingFactory2 interface [Windows Imaging Component]","IWICImagingFactory2 interface [Windows Imaging Component]","described","wic.iwicimagingfactory2","wincodec/IWICImagingFactory2"]
old-location: wic\iwicimagingfactory2.htm
tech.root: wic
ms.assetid: 95F64E01-6174-4C1C-B0BE-331380E583C2
ms.date: 12/05/2018
ms.keywords: IWICImagingFactory2, IWICImagingFactory2 interface [Windows Imaging Component], IWICImagingFactory2 interface [Windows Imaging Component],described, wic.iwicimagingfactory2, wincodec/IWICImagingFactory2
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
 - IWICImagingFactory2
 - wincodec/IWICImagingFactory2
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
 - IWICImagingFactory2
---

# IWICImagingFactory2 interface


## -description

An extension of the WIC factory interface that includes the ability to create an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder">IWICImageEncoder</a>.  This interface uses a <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> device and an input image to encode to a destination <a href="/windows/desktop/wic/-wic-imp-iwicbitmapencoder">IWICBitmapEncoder</a>.

## -inheritance

The <b>IWICImagingFactory2</b> interface inherits from <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>. <b>IWICImagingFactory2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>
