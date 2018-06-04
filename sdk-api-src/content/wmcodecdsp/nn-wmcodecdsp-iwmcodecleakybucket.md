---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWMCodecLeakyBucket interface


## -description


Configures the "leaky bucket" parameters on a video encoder.

This interface is implemented by all of the encoder objects. You can get a pointer to the <b>IWMCodecLeakyBucket</b> interface for a Windows Media video encoder by calling the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method of any other interface on the object, such as <a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject</a> or <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>. This interface is not  implemented on any of the decoders.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecLeakyBucket</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMCodecLeakyBucket</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecLeakyBucket</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46eee8c9-e10e-41e3-9400-051b4484eee0">GetBufferFullnessBits</a>
</td>
<td align="left" width="63%">
Not implemented in this release.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fa0835e-7386-4032-a94b-ef52259aeea9">GetBufferSizeBits</a>
</td>
<td align="left" width="63%">
Retrieves the  current size of the buffer in bits.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e82badb3-64a8-40f0-9c51-bb2539f242f2">SetBufferFullnessBits</a>
</td>
<td align="left" width="63%">
Not  implemented in this release.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b602e8ca-8446-4f94-bcd0-193084d96565">SetBufferSizeBits</a>
</td>
<td align="left" width="63%">
Sets the buffer size in bits.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/2f7f80d6-3abb-462f-a571-b223a1d59da6">The Leaky Bucket Buffer Model</a>
 

 

