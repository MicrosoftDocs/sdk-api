---
UID: NN:wincodec.IWICPlanarBitmapSourceTransform
title: IWICPlanarBitmapSourceTransform (wincodec.h)
description: Provides access to planar Y’CbCr pixel formats where pixel components are stored in separate component planes.helpviewer_keywords: ["IWICPlanarBitmapSourceTransform","IWICPlanarBitmapSourceTransform interface [Windows Imaging Component]","IWICPlanarBitmapSourceTransform interface [Windows Imaging Component]","described","wic.iwicplanarbitmapsourcetransform","wincodec/IWICPlanarBitmapSourceTransform"]
old-location: wic\iwicplanarbitmapsourcetransform.htm
tech.root: wic
ms.assetid: AA47F10A-C90A-4DAF-973F-2669D7364CB9
ms.date: 12/05/2018
ms.keywords: IWICPlanarBitmapSourceTransform, IWICPlanarBitmapSourceTransform interface [Windows Imaging Component], IWICPlanarBitmapSourceTransform interface [Windows Imaging Component],described, wic.iwicplanarbitmapsourcetransform, wincodec/IWICPlanarBitmapSourceTransform
f1_keywords:
- wincodec/IWICPlanarBitmapSourceTransform
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windowscodecs.dll
api_name:
- IWICPlanarBitmapSourceTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICPlanarBitmapSourceTransform interface


## -description


Provides access to planar Y’CbCr pixel formats where pixel components are stored in separate component planes.  This interface also allows access to other codec optimizations for flip/rotate, scale, and format conversion to other Y’CbCr planar formats; this is similar to the pre-existing <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsourcetransform">IWICBitmapSourceTransform</a> interface.

QueryInterface can be used to obtain this interface from the Windows provided implementations of <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a> for the JPEG decoder, <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler">IWICBitmapScaler</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapfliprotator">IWICBitmapFlipRotator</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwiccolortransform">IWICColorTransform</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICPlanarBitmapSourceTransform</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICPlanarBitmapSourceTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICPlanarBitmapSourceTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels">CopyPixels</a>
</td>
<td align="left" width="63%">
Copies pixels into the destination planes.  Configured by the supplied input parameters.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform">DoesSupportTransform</a>
</td>
<td align="left" width="63%">
Use this method to determine if a desired planar output is supported and allow the caller to choose an optimized code path if it is.  

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wic/jpeg-ycbcr-support">JPEG YCbCr Support</a>
 

 

