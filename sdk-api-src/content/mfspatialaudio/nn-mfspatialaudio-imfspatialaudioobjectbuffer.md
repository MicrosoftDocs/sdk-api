---
UID: NN:mfspatialaudio.IMFSpatialAudioObjectBuffer
title: IMFSpatialAudioObjectBuffer
author: windows-sdk-content
description: Represents a section of audio data with associated positional and rendering metadata. Spatial audio objects are stored in IMFSpatialAudioSample instances, and allow passing of spatial audio information between Media Foundation components.
old-location: mf\imfspatialaudioobjectbuffer.htm
tech.root: medfound
ms.assetid: 61E9BC6A-2120-4874-9053-E1D232DF1CCA
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFSpatialAudioObjectBuffer, IMFSpatialAudioObjectBuffer interface [Media Foundation], IMFSpatialAudioObjectBuffer interface [Media Foundation],described, mf.imfspatialaudioobjectbuffer, mfspatialaudio/IMFSpatialAudioObjectBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfspatialaudio.h
req.include-header: Mfobjects.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.lib
 - mfobjects.dll
api_name:
 - IMFSpatialAudioObjectBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/5BB0DEB2-B3B9-4723-973D-A9296D94DDE6">GetID</a>
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
<a href="https://msdn.microsoft.com/CF0285D2-E56B-44A5-B7E0-3227213D9523">GetType</a>
</td>
<td align="left" width="63%">
Gets the type of the spatial audio object represented by the buffer. If <a href="https://msdn.microsoft.com/3D21D093-FDCE-4ECA-B8B2-56D6E5D5D9C6">SetType</a> has not been called previously, this method returns the default value of <b>AudioObjectType_None</b>.

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
<a href="https://msdn.microsoft.com/3D21D093-FDCE-4ECA-B8B2-56D6E5D5D9C6">SetType</a>
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
 

 

