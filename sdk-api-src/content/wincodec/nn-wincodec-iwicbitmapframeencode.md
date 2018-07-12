---
UID: NN:wincodec.IWICBitmapFrameEncode
title: IWICBitmapFrameEncode
author: windows-sdk-content
description: Represents an encoder's individual image frames.
old-location: wic\_wic_codec_iwicbitmapframeencode.htm
old-project: wic
ms.assetid: a8de774b-3783-46be-9a21-c9fec2f10ffd
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IWICBitmapFrameEncode, IWICBitmapFrameEncode interface [Windows Imaging Component], IWICBitmapFrameEncode interface [Windows Imaging Component],described, _wic_codec_iwicbitmapframeencode, wic._wic_codec_iwicbitmapframeencode, wincodec/IWICBitmapFrameEncode
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
 - Windowscodecs.dll
api_name:
 - IWICBitmapFrameEncode
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapFrameEncode interface


## -description


Represents an encoder's individual image frames.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICBitmapFrameEncode</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICBitmapFrameEncode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICBitmapFrameEncode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Commits the frame to the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ff79820-5f44-4262-b97f-df783829e44b">GetMetadataQueryWriter</a>
</td>
<td align="left" width="63%">
Gets the metadata query writer for the encoder frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the frame encoder using the given properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c955dede-297f-44c1-aa03-31a07a6d69d2">SetColorContexts</a>
</td>
<td align="left" width="63%">
Sets a given number <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> profiles to the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c463fc95-695d-4ba3-bf62-5b09d69c60c2">SetPalette</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a> for indexed pixel formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9327b5dd-18a3-40c6-8bb4-245fcc7fb582">SetPixelFormat</a>
</td>
<td align="left" width="63%">
Requests that the encoder use the specified pixel format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b9e564a-5278-41d7-84ab-8b7594e776c7">SetResolution</a>
</td>
<td align="left" width="63%">
Sets the physical resolution of the output image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439729">SetSize</a>
</td>
<td align="left" width="63%">
Sets the output image dimensions for the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da6924cf-87c0-4774-a02e-5d54be65ef28">SetThumbnail</a>
</td>
<td align="left" width="63%">
Sets the frame thumbnail if supported by the codec.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b430fe0-5230-47dc-95c0-aeabd138cefe">WritePixels</a>
</td>
<td align="left" width="63%">
Encodes the frame scanlines.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc748982-6dc8-41cc-a23b-9d127dc22a1f">WriteSource</a>
</td>
<td align="left" width="63%">
Encodes a bitmap source.

</td>
</tr>
</table> 


## -see-also




<a href="http://msdn.microsoft.com/en-us/library/ms771770.aspx">AITCodec Sample CODEC</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/2be5cfeb-2dd3-4486-b639-35ee28a7dd7b">WIC GUIDs and CLSIDs</a>



<a href="https://msdn.microsoft.com/a05b496a-bd4c-4065-8060-df0f8930cde7">Windows Imaging Component Overview</a>
 

 

