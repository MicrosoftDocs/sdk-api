---
UID: NN:rdpencomapi.IRDPSRAPIAudioStream
title: IRDPSRAPIAudioStream
author: windows-sdk-content
description: Enables sending an audio stream from the collaboration sharer Microsoft ActiveX control to collaboration viewer controls.
old-location: rdp\irdpsrapiaudiostream.htm
old-project: rdp
ms.assetid: B2BC04A1-DE22-4543-9F10-33B0B99E0F92
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IRDPSRAPIAudioStream, IRDPSRAPIAudioStream class [RDP], IRDPSRAPIAudioStream class [RDP],described, rdp.irdpsrapiaudiostream, rdpencomapi/IRDPSRAPIAudioStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIAudioStream
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: ADAM
---

# IRDPSRAPIAudioStream interface


## -description


Enables sending an audio stream from the collaboration sharer Microsoft ActiveX control to 
    collaboration viewer controls. This interface only supports a pulse code modulation (PCM) audio stream 
    with the following specifications; 44.1 kHz, 2 channels, 16 bits/sample.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIAudioStream</b> class inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRDPSRAPIAudioStream</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/03926ABF-D5D0-4D13-B081-0085EC698E9F">FreeBuffer</a>
</td>
<td align="left" width="63%">
Releases the hold on the buffer after the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a> method is  called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a>
</td>
<td align="left" width="63%">
Gets audio data from the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Starts the audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops the audio stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bb1df622-bfcd-4d84-b5f6-780b693cc760">Windows Desktop Sharing Interfaces</a>
 

 

