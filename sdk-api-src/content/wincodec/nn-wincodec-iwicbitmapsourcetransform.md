---
UID: NN:wincodec.IWICBitmapSourceTransform
title: IWICBitmapSourceTransform (wincodec.h)
description: Exposes methods for offloading certain operations to the underlying IWICBitmapSource implementation.
old-location: wic\_wic_codec_iwicbitmapsourcetransform.htm
tech.root: wic
ms.assetid: f9cc348f-d4f0-4e77-90d6-9ff563a1799c
ms.date: 12/05/2018
ms.keywords: IWICBitmapSourceTransform, IWICBitmapSourceTransform interface [Windows Imaging Component], IWICBitmapSourceTransform interface [Windows Imaging Component],described, _wic_codec_iwicbitmapsourcetransform, wic._wic_codec_iwicbitmapsourcetransform, wincodec/IWICBitmapSourceTransform
f1_keywords:
- wincodec/IWICBitmapSourceTransform
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windowscodecs.lib
- Windowscodecs.dll
api_name:
- IWICBitmapSourceTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapSourceTransform interface


## -description


Exposes methods for offloading certain operations to the underlying <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> implementation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapSourceTransform</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICBitmapSourceTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapSourceTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels">CopyPixels</a>
</td>
<td align="left" width="63%">
Copies pixel data using the supplied input parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform">DoesSupportTransform</a>
</td>
<td align="left" width="63%">
Determines whether a specific transform option is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat">GetClosestPixelFormat</a>
</td>
<td align="left" width="63%">
Retrieves the closest pixel format supported given a desired format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize">GetClosestSize</a>
</td>
<td align="left" width="63%">
Returns the closest dimensions the implementation can natively scale to given the desired dimensions.

</td>
</tr>
</table> 


## -remarks



The <b>IWICBitmapSourceTransform</b> interface is implemented by codecs which can natively scale, flip, rotate, or format convert pixels during decoding. As the transformation is combined with the decoding process, native transformation will generally offer performance advantages over non-native transformations. The inbox <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler">IWICBitmapScaler</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapfliprotator">IWICBitmapFlipRotator</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter">IWICFormatConverter</a> implementations all make use of the <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a> interface when they are placed immediately after a supported <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-imp-iwicbitmapframedecode">IWICBitmapFrameDecode</a>, so in the typical case an application will automatically receive this performance increase and does not need to directly use this interface. However, when chaining multiple transformations, or when implementing a custom transformation, there may be a performance advantage to using the IWICBitmapSourceTransform interface directly.




