---
UID: NN:audioengineendpoint.IAudioEndpointOffloadStreamMute
title: IAudioEndpointOffloadStreamMute (audioengineendpoint.h)

description: The IAudioEndpointOffloadStreamMute interface allows a client to manipulate the mute status of the offloaded audio stream.
old-location: coreaudio\iaudioendpointoffloadstreammute.htm
tech.root: CoreAudio
ms.assetid: F102CBB2-6751-416C-B59B-F91440583594

ms.date: 12/05/2018
ms.keywords: IAudioEndpointOffloadStreamMute, IAudioEndpointOffloadStreamMute interface [Core Audio], IAudioEndpointOffloadStreamMute interface [Core Audio],described, audioengineendpoint/IAudioEndpointOffloadStreamMute, coreaudio.iaudioendpointoffloadstreammute
ms.topic: interface
f1_keywords: 
 - "audioengineendpoint/IAudioEndpointOffloadStreamMute"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointOffloadStreamMute interface


## -description


The <b>IAudioEndpointOffloadStreamMute</b> interface allows a client to manipulate the mute status of the offloaded audio stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioEndpointOffloadStreamMute</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioEndpointOffloadStreamMute</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointoffloadstreammute-getmute">GetMute</a>
</td>
<td align="left" width="63%">
Indicates whether the offloaded stream is muted or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpointoffloadstreammute-setmute">SetMute</a>
</td>
<td align="left" width="63%">
Sets the mute status of the offloaded stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>
 

 

