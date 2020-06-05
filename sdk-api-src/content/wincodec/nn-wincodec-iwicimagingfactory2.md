---
UID: NN:wincodec.IWICImagingFactory2
title: IWICImagingFactory2 (wincodec.h)
description: An extension of the WIC factory interface that includes the ability to create an IWICImageEncoder.helpviewer_keywords: ["IWICImagingFactory2","IWICImagingFactory2 interface [Windows Imaging Component]","IWICImagingFactory2 interface [Windows Imaging Component]","described","wic.iwicimagingfactory2","wincodec/IWICImagingFactory2"]
old-location: wic\iwicimagingfactory2.htm
tech.root: wic
ms.assetid: 95F64E01-6174-4C1C-B0BE-331380E583C2
ms.date: 12/05/2018
ms.keywords: IWICImagingFactory2, IWICImagingFactory2 interface [Windows Imaging Component], IWICImagingFactory2 interface [Windows Imaging Component],described, wic.iwicimagingfactory2, wincodec/IWICImagingFactory2
f1_keywords:
- wincodec/IWICImagingFactory2
dev_langs:
- c++
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
- IWICImagingFactory2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICImagingFactory2 interface


## -description


An extension of the WIC factory interface that includes the ability to create an <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder">IWICImageEncoder</a>.  This interface uses a <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> device and an input image to encode to a destination <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapencoder">IWICBitmapEncoder</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICImagingFactory2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>. <b>IWICImagingFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICImagingFactory2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder">CreateImageEncoder</a>
</td>
<td align="left" width="63%">
Creates a new image encoder object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>
 

 

