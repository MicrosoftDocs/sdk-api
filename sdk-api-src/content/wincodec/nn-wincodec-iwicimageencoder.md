---
UID: NN:wincodec.IWICImageEncoder
title: IWICImageEncoder (wincodec.h)
author: windows-sdk-content
description: Encodes ID2D1Image interfaces to an IWICBitmapEncoder.
old-location: wic\iwicimageencoder.htm
tech.root: wic
ms.assetid: D9854D82-0226-4DD8-AE54-93E5B6544B46
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICImageEncoder, IWICImageEncoder interface [Windows Imaging Component], IWICImageEncoder interface [Windows Imaging Component],described, wic.iwicimageencoder, wincodec/IWICImageEncoder
ms.topic: interface
f1_keywords: ["wincodec/IWICImageEncoder"]
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
 - IWICImageEncoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICImageEncoder interface


## -description


Encodes <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a> interfaces to an <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapencoder">IWICBitmapEncoder</a>.  The input images can be larger than the maximum device texture size.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICImageEncoder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICImageEncoder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICImageEncoder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicimageencoder-writeframe">WriteFrame</a>
</td>
<td align="left" width="63%">
Encodes the image to the frame given by the <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicimageencoder-writeframethumbnail">WriteFrameThumbnail</a>
</td>
<td align="left" width="63%">
Encodes the image as a thumbnail to the frame given by the <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapframeencode">IWICBitmapFrameEncode</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicimageencoder-writethumbnail">WriteThumbnail</a>
</td>
<td align="left" width="63%">
Encodes the given image as the thumbnail to the given WIC bitmap encoder.

</td>
</tr>
</table> 

