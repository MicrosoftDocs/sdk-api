---
UID: NN:audioengineendpoint.IAudioEndpointOffloadStreamMute
title: IAudioEndpointOffloadStreamMute
author: windows-sdk-content
description: The IAudioEndpointOffloadStreamMute interface allows a client to manipulate the mute status of the offloaded audio stream.
old-location: coreaudio\iaudioendpointoffloadstreammute.htm
tech.root: CoreAudio
ms.assetid: F102CBB2-6751-416C-B59B-F91440583594
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAudioEndpointOffloadStreamMute, IAudioEndpointOffloadStreamMute interface [Core Audio], IAudioEndpointOffloadStreamMute interface [Core Audio],described, audioengineendpoint/IAudioEndpointOffloadStreamMute, coreaudio.iaudioendpointoffloadstreammute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioengineendpoint.h
api_name:
 - IAudioEndpointOffloadStreamMute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointOffloadStreamMute interface


## -description


The <b>IAudioEndpointOffloadStreamMute</b> interface allows a client to manipulate the mute status of the offloaded audio stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointOffloadStreamMute</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioEndpointOffloadStreamMute</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpointOffloadStreamMute</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0A8F254B-1287-4633-A14D-7F620CB64818">GetMute</a>
</td>
<td align="left" width="63%">
Indicates whether the offloaded stream is muted or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43AF8146-BDF6-47F5-BD8F-DA46C4624D95">SetMute</a>
</td>
<td align="left" width="63%">
Sets the mute status of the offloaded stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>
 

 

