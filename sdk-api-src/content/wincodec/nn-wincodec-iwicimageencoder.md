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
---

# IWICImageEncoder interface


## -description


Encodes <a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a> interfaces to an <a href="https://msdn.microsoft.com/b671e941-ded6-4bde-bc4d-461f13feade0">IWICBitmapEncoder</a>.  The input images can be larger than the maximum device texture size.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICImageEncoder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICImageEncoder</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/08CD0CE4-5948-4A8F-AA96-9A2BF43EC6D3">WriteFrame</a>
</td>
<td align="left" width="63%">
Encodes the image to the frame given by the <a href="https://msdn.microsoft.com/509fa49c-c90d-4270-a338-6ce638ccd89a">IWICBitmapFrameEncode</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5A34F900-73F1-4FFC-B251-F22E0EDDB873">WriteFrameThumbnail</a>
</td>
<td align="left" width="63%">
Encodes the image as a thumbnail to the frame given by the <a href="https://msdn.microsoft.com/509fa49c-c90d-4270-a338-6ce638ccd89a">IWICBitmapFrameEncode</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/322AD13D-E755-45BD-A31D-D603DBD7FA81">WriteThumbnail</a>
</td>
<td align="left" width="63%">
Encodes the given image as the thumbnail to the given WIC bitmap encoder.

</td>
</tr>
</table> 

