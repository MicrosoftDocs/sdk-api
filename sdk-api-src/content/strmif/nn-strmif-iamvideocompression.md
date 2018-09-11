---
UID: NN:strmif.IAMVideoCompression
title: IAMVideoCompression
author: windows-sdk-content
description: The IAMVideoCompression interface sets and retrieves video compression properties.
old-location: dshow\iamvideocompression.htm
tech.root: DirectShow
ms.assetid: 6b7d8a98-35b8-442f-bf51-9e66fd03e2c9
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMVideoCompression, IAMVideoCompression interface [DirectShow], IAMVideoCompression interface [DirectShow],described, IAMVideoCompressionInterface, dshow.iamvideocompression, strmif/IAMVideoCompression
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoCompression
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoCompression interface


## -description



The <b>IAMVideoCompression</b> interface sets and retrieves video compression properties. It is supported by some video compression filters, and also by some video capture filters that output compressed video. Filters that support this interface expose it through their output pins.

An application can use this interface to control how video is compressed, including characteristics such as the key-frame rate or the compression quality.

A filter that supports this interface might not support every method. Use the <a href="https://msdn.microsoft.com/d8ba2ba2-510a-4fb8-844e-48059ec4ef0d">IAMVideoCompression::GetInfo</a> method to determine which methods the filter supports.

<div class="alert"><b>Note</b>  To use this interface on a capture filter, you might need to connect the filter to another filter in the graph.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMVideoCompression</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMVideoCompression</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMVideoCompression</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af73cfaa-3297-44a7-96a7-8805aad057e2">get_KeyFrameRate</a>
</td>
<td align="left" width="63%">
Retrieves the key-frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/621292dd-42d9-4458-8971-929db39ed8b9">get_PFramesPerKeyFrame</a>
</td>
<td align="left" width="63%">
Retrieves the P frame frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a34b6d15-3c84-476e-bd2f-ee10b59ded82">get_Quality</a>
</td>
<td align="left" width="63%">
Retrieves the compression quality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f12aa72-3468-4dca-a5f6-43f64f6d2f83">get_WindowSize</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames over which the compressor must maintain an average data rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8ba2ba2-510a-4fb8-844e-48059ec4ef0d">GetInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the filter's compression properties, including capabilities and default values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19f5d231-965e-4b0a-bd0b-e85b03d79c71">OverrideFrameSize</a>
</td>
<td align="left" width="63%">
Overrides a particular frame's data rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e8e52b9-cc66-42f5-a0ea-110188bfcf8b">OverrideKeyFrame</a>
</td>
<td align="left" width="63%">
Forces a particular frame to be a key frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc229333-3524-4228-ab13-a6e9619643fd">put_KeyFrameRate</a>
</td>
<td align="left" width="63%">
Sets the key-frame rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf1dfc28-a6c7-4c0d-96ea-8cf417b13a10">put_PFramesPerKeyFrame</a>
</td>
<td align="left" width="63%">
Sets the predicted (P) frame frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ecc00f9-73d4-4d26-b7b0-1b6419027d69">put_Quality</a>
</td>
<td align="left" width="63%">
Sets the compression quality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/744cd32d-5f61-4069-82c4-50bc1b800f24">put_WindowSize</a>
</td>
<td align="left" width="63%">
Sets the number of frames over which the compressor must maintain an average data rate.

</td>
</tr>
</table> 


## -remarks



For Windows Driver Model (WDM) devices, the <a href="https://msdn.microsoft.com/97432b99-e89b-4d69-963d-a959f887e580">WDM Video Capture Filter</a> automatically exposes this interface if the WDM driver supports the <a href="https://msdn.microsoft.com/7af6f7f0-d446-4b44-9423-efd37f731e0b">PROPSETID_VIDCAP_VIDEOCOMPRESSION</a> property set. For more information, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=181442">Windows Driver Kit (WDK)</a> documentation.




## -see-also




<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

