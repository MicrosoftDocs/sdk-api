---
UID: NN:audioengineendpoint.IAudioEndpoint
title: IAudioEndpoint (audioengineendpoint.h)
description: Provides information to the audio engine about an audio endpoint. This interface is implemented by an audio endpoint.
old-location: termserv\iaudioendpoint.htm
tech.root: TermServ
ms.assetid: a1bb3fe4-6051-4b9c-8270-70375e700f01
ms.date: 12/05/2018
ms.keywords: IAudioEndpoint, IAudioEndpoint interface [Remote Desktop Services], IAudioEndpoint interface [Remote Desktop Services],described, audioengineendpoint/IAudioEndpoint, termserv.iaudioendpoint
f1_keywords:
- audioengineendpoint/IAudioEndpoint
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpoint interface


## -description


Provides information to the audio engine about an audio endpoint. This interface is implemented by an 
    audio endpoint.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpoint</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpoint</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-getframeformat">GetFrameFormat</a>
</td>
<td align="left" width="63%">
Retrieves the format of the endpoint.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-getframesperpacket">GetFramesPerPacket</a>
</td>
<td align="left" width="63%">
Gets the maximum number of frames per packet that the audio endpoint can support, based on the period and 
     the sample rate of the current stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-getlatency">GetLatency</a>
</td>
<td align="left" width="63%">
Gets the latency of the audio endpoint.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-seteventhandle">SetEventHandle</a>
</td>
<td align="left" width="63%">
Sets the handle for the event  that the audio engine uses to signal the client when the audio engine 
     finishes processing the audio buffer. The audio engine uses this method only when the endpoint is event 
     driven.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-setstreamflags">SetStreamFlags</a>
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




<a href="https://docs.microsoft.com/windows/desktop/TermServ/terminal-services-audioendpoint-api-reference">Remote Desktop Services AudioEndpoint API Reference</a>
 

 

