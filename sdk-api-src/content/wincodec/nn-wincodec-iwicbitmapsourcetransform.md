---
UID: NN:wincodec.IWICBitmapSourceTransform
title: IWICBitmapSourceTransform
author: windows-sdk-content
description: Exposes methods for offloading certain operations to the underlying IWICBitmapSource implementation.
old-location: wic\_wic_codec_iwicbitmapsourcetransform.htm
old-project: wic
ms.assetid: f9cc348f-d4f0-4e77-90d6-9ff563a1799c
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICBitmapSourceTransform, IWICBitmapSourceTransform interface [Windows Imaging Component], IWICBitmapSourceTransform interface [Windows Imaging Component],described, _wic_codec_iwicbitmapsourcetransform, wic._wic_codec_iwicbitmapsourcetransform, wincodec/IWICBitmapSourceTransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICTiffCompressionOption
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
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapSourceTransform interface


## -description


Exposes methods for offloading certain operations to the underlying <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> implementation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapSourceTransform</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICBitmapSourceTransform</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c4c36750-bf30-4e58-aca6-bbb49c7cde4b">CopyPixels</a>
</td>
<td align="left" width="63%">
Copies pixel data using the supplied input parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73f27e20-3245-42b3-8b83-29c3c969624f">DoesSupportTransform</a>
</td>
<td align="left" width="63%">
Determines whether a specific transform option is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/153c5e2a-c42f-4949-9313-48d5e186ecf3">GetClosestPixelFormat</a>
</td>
<td align="left" width="63%">
Retrieves the closest pixel format supported given a desired format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0eae79dc-d636-4449-ba90-0f296b71573a">GetClosestSize</a>
</td>
<td align="left" width="63%">
Returns the closest dimensions the implementation can natively scale to given the desired dimensions.

</td>
</tr>
</table> 


## -remarks



The <b>IWICBitmapSourceTransform</b> interface is implemented by codecs which can natively scale, flip, rotate, or format convert pixels during decoding. As the transformation is combined with the decoding process, native transformation will generally offer performance advantages over non-native transformations. The inbox <a href="https://msdn.microsoft.com/cc14be9d-d750-40db-a95f-309b392cefe8">IWICBitmapScaler</a>, <a href="https://msdn.microsoft.com/1fcb19ba-34bd-48c0-9964-0c973c31cacc">IWICBitmapFlipRotator</a>, and <a href="https://msdn.microsoft.com/d558aaa7-5962-424c-9e83-363fba09ad50">IWICFormatConverter</a> implementations all make use of the <a href="https://msdn.microsoft.com/6a3e682c-55c6-4728-9d14-5eb0290f3dcc">IWICBitmapSourceTransform</a> interface when they are placed immediately after a supported <a href="https://msdn.microsoft.com/7dc626ad-1158-4b67-8ca7-47b4cf88e278">IWICBitmapFrameDecode</a>, so in the typical case an application will automatically receive this performance increase and does not need to directly use this interface. However, when chaining multiple transformations, or when implementing a custom transformation, there may be a performance advantage to using the IWICBitmapSourceTransform interface directly.




