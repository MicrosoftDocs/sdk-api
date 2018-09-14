---
UID: NN:audioengineendpoint.IAudioEndpoint
title: IAudioEndpoint
author: windows-sdk-content
description: Provides information to the audio engine about an audio endpoint. This interface is implemented by an audio endpoint.
old-location: termserv\iaudioendpoint.htm
tech.root: TermServ
ms.assetid: a1bb3fe4-6051-4b9c-8270-70375e700f01
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAudioEndpoint, IAudioEndpoint interface [Remote Desktop Services], IAudioEndpoint interface [Remote Desktop Services],described, audioengineendpoint/IAudioEndpoint, termserv.iaudioendpoint
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - Audioengineendpoint.h
api_name:
 - IAudioEndpoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpoint interface


## -description


Provides information to the audio engine about an audio endpoint. This interface is implemented by an 
    audio endpoint.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpoint</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioEndpoint</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioEndpoint</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb34ef19-4155-461e-a8d7-0a903e9d7c72">GetFrameFormat</a>
</td>
<td align="left" width="63%">
Retrieves the format of the endpoint.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9e47262-9e6f-4ddf-a74a-b7fa63983a5a">GetFramesPerPacket</a>
</td>
<td align="left" width="63%">
Gets the maximum number of frames per packet that the audio endpoint can support, based on the period and 
     the sample rate of the current stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9afca6b7-2e0e-40a1-bb4a-932dad21b9eb">GetLatency</a>
</td>
<td align="left" width="63%">
Gets the latency of the audio endpoint.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f0f216a-d785-42e9-b07d-f1f2568b5833">SetEventHandle</a>
</td>
<td align="left" width="63%">
Sets the handle for the event  that the audio engine uses to signal the client when the audio engine 
     finishes processing the audio buffer. The audio engine uses this method only when the endpoint is event 
     driven.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6713912-ba7e-4e3e-95d9-8318c40a7042">SetStreamFlags</a>
</td>
<td align="left" width="63%">
Sets the stream  configuration flags on the audio endpoint.

</td>
</tr>
</table> 


## -remarks



The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client 
    applications.




## -see-also




<a href="https://msdn.microsoft.com/0e3ea0e7-8c61-400e-b8ef-8a0403aedafa">Remote Desktop Services AudioEndpoint API Reference</a>
 

 

