---
UID: NN:wincodec.IWICImagingFactory2
title: IWICImagingFactory2
author: windows-sdk-content
description: An extension of the WIC factory interface that includes the ability to create an IWICImageEncoder.
old-location: wic\iwicimagingfactory2.htm
tech.root: wic
ms.assetid: 95F64E01-6174-4C1C-B0BE-331380E583C2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWICImagingFactory2, IWICImagingFactory2 interface [Windows Imaging Component], IWICImagingFactory2 interface [Windows Imaging Component],described, wic.iwicimagingfactory2, wincodec/IWICImagingFactory2
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICImagingFactory2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICImagingFactory2 interface


## -description


An extension of the WIC factory interface that includes the ability to create an <a href="https://msdn.microsoft.com/D9854D82-0226-4DD8-AE54-93E5B6544B46">IWICImageEncoder</a>.  This interface uses a <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> device and an input image to encode to a destination <a href="https://msdn.microsoft.com/b671e941-ded6-4bde-bc4d-461f13feade0">IWICBitmapEncoder</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICImagingFactory2</b> interface inherits from <a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>. <b>IWICImagingFactory2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1F75030F-68B0-4333-B3CF-C4ABD8969448">CreateImageEncoder</a>
</td>
<td align="left" width="63%">
Creates a new image encoder object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>
 

 

