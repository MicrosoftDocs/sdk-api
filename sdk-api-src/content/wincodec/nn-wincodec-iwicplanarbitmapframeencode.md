---
UID: NN:wincodec.IWICPlanarBitmapFrameEncode
title: IWICPlanarBitmapFrameEncode
author: windows-sdk-content
description: Allows planar component image pixels to be written to an encoder.
old-location: wic\iwicplanarbitmapframeencode.htm
old-project: wic
ms.assetid: 7ACA58CC-E132-4836-B955-322375ADDAA1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWICPlanarBitmapFrameEncode, IWICPlanarBitmapFrameEncode interface [Windows Imaging Component], IWICPlanarBitmapFrameEncode interface [Windows Imaging Component],described, wic.iwicplanarbitmapframeencode, wincodec/IWICPlanarBitmapFrameEncode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICPlanarBitmapFrameEncode
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICPlanarBitmapFrameEncode interface


## -description


Allows planar component image pixels to be written to an encoder.   When supported by the encoder, this allows an application to encode planar component image data without first converting to an interleaved pixel format.

You can use

QueryInterface to obtain this interface from the Windows provided implementation of <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a> for the JPEG encoder.  



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICPlanarBitmapFrameEncode</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICPlanarBitmapFrameEncode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICPlanarBitmapFrameEncode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57DB1340-9BE4-46ED-9ADE-9B91657F09B7">WritePixels</a>
</td>
<td align="left" width="63%">
Writes lines from the source planes to the encoded format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/220D9216-1053-48E1-B7FD-5E3E46001562">WriteSource</a>
</td>
<td align="left" width="63%">
Writes lines from the source planes to the encoded format.

</td>
</tr>
</table> 


## -remarks



Encoding YCbCr data using <b>IWICPlanarBitmapFrameEncode</b> is similar but not identical to encoding interleaved data using <a href="https://msdn.microsoft.com/509fa49c-c90d-4270-a338-6ce638ccd89a">IWICBitmapFrameEncode</a>. The planar interface only exposes the ability to write planar frame image data, and you should continue to use the frame encode interface to set metadata or a thumbnail and to commit at the end of the operation.





## -see-also




<a href="https://msdn.microsoft.com/50B89A96-72E8-4771-9109-207F4CDD06CB">JPEG YCbCr Support</a>
 

 

