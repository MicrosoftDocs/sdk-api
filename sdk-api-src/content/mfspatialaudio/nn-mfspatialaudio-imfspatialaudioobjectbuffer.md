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

# IMFSpatialAudioObjectBuffer interface


## -description


Represents a section of audio data with
associated positional and rendering metadata.  Spatial audio objects are stored in <a href="https://msdn.microsoft.com/EA0277BF-C9C8-42FE-9206-A87FC3C50A9F">IMFSpatialAudioSample</a> instances, and allow passing of 
spatial audio information between Media Foundation components.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSpatialAudioObjectBuffer</b> interface inherits from <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a>. <b>IMFSpatialAudioObjectBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSpatialAudioObjectBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546827">GetID</a>
</td>
<td align="left" width="63%">
Returns the unique, unsigned 32-bit ID of the spatial audio object represented by the buffer.
    If <a href="https://msdn.microsoft.com/01979492-2CA1-4DAA-8B03-720B521C2D9A">SetID</a> method was not previously called, this method returns the invalid object ID, -1 
    (0xffffffff).  The invalid ID indicates that the object buffer is unused and
    contains invalid data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19BF7AC6-B21F-47D1-8573-48C5E4869574">GetMetadataItems</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to a buffer that may 
    contain spatial audio metadata.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Gets the type of the spatial audio object represented by the buffer. If <a href="https://msdn.microsoft.com/library/windows/hardware/jj991816">SetType</a> has not been called previously, this method returns the default value of <b>AudioObjectType_None</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01979492-2CA1-4DAA-8B03-720B521C2D9A">SetID</a>
</td>
<td align="left" width="63%">
Sets the ID of the spatial audio object represented by the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991816">SetType</a>
</td>
<td align="left" width="63%">
Sets the type of the spatial audio object represented by the buffer.

</td>
</tr>
</table> 


## -remarks



To get the audio data contained in the spatial audio object, use the    <a href="https://msdn.microsoft.com/28ac372a-6e73-4e66-bf69-bcc244821b71">IMFMediaBuffer::Lock</a> and <a href="https://msdn.microsoft.com/3ca53321-5533-45f0-b415-6a16f780ec54">IMFMediaBuffer::Unlock</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a>
 

 

