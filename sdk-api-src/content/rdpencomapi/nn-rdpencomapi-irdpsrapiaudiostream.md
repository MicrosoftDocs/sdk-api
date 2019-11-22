---
UID: NN:rdpencomapi.IRDPSRAPIAudioStream
title: IRDPSRAPIAudioStream (rdpencomapi.h)

description: Enables sending an audio stream from the collaboration sharer Microsoft ActiveX control to collaboration viewer controls.
old-location: rdp\irdpsrapiaudiostream.htm
tech.root: rdp
ms.assetid: B2BC04A1-DE22-4543-9F10-33B0B99E0F92

ms.date: 12/05/2018
ms.keywords: IRDPSRAPIAudioStream, IRDPSRAPIAudioStream class [RDP], IRDPSRAPIAudioStream class [RDP],described, rdp.irdpsrapiaudiostream, rdpencomapi/IRDPSRAPIAudioStream
ms.topic: interface
f1_keywords: 
 - "rdpencomapi/IRDPSRAPIAudioStream"
dev_langs:
 - c++
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIAudioStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRDPSRAPIAudioStream interface


## -description


Enables sending an audio stream from the collaboration sharer Microsoft ActiveX control to 
    collaboration viewer controls. This interface only supports a pulse code modulation (PCM) audio stream 
    with the following specifications; 44.1 kHz, 2 channels, 16 bits/sample.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIAudioStream</b> class inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRDPSRAPIAudioStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRDPSRAPIAudioStream</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-freebuffer">FreeBuffer</a>
</td>
<td align="left" width="63%">
Releases the hold on the buffer after the 
     <a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-getbuffer">GetBuffer</a> method is  called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-getbuffer">GetBuffer</a>
</td>
<td align="left" width="63%">
Gets audio data from the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-start">Start</a>
</td>
<td align="left" width="63%">
Starts the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops the audio stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/rdp/windows-desktop-sharing-interfaces">Windows Desktop Sharing Interfaces</a>
 

 

