---
UID: NN:audioengineendpoint.IAudioDeviceEndpoint
title: IAudioDeviceEndpoint (audioengineendpoint.h)
description: Initializes a device endpoint object and gets the capabilities of the device that it represents.
old-location: termserv\iaudiodeviceendpoint.htm
tech.root: TermServ
ms.assetid: 3112bc7e-e138-4b42-8f82-61fdf19f7e94
ms.date: 12/05/2018
ms.keywords: IAudioDeviceEndpoint, IAudioDeviceEndpoint interface [Remote Desktop Services], IAudioDeviceEndpoint interface [Remote Desktop Services],described, audioengineendpoint/IAudioDeviceEndpoint, termserv.iaudiodeviceendpoint
ms.topic: interface
f1_keywords:
- audioengineendpoint/IAudioDeviceEndpoint
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
- IAudioDeviceEndpoint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioDeviceEndpoint interface


## -description


Initializes a device endpoint object and gets the capabilities of the device that it represents.

A <i>device endpoint</i> abstracts an audio device. The device can be a rendering device such as a speaker or a capture  device such as a microphone. A device endpoint must implement the <b>IAudioDeviceEndpoint</b> interface.
      

To a get a reference to the <b>IAudioDeviceEndpoint</b> interface of the device, the audio engine calls <b>QueryInterface</b> on the audio endpoint (<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt">IAudioInputEndpointRT</a> or <a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt">IAudioOutputEndpointRT</a>) for the device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioDeviceEndpoint</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioDeviceEndpoint</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioDeviceEndpoint</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudiodeviceendpoint-geteventdrivencapable">GetEventDrivenCapable</a>
</td>
<td align="left" width="63%">
Indicates whether the audio endpoint can be event driven.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudiodeviceendpoint-getrtcaps">GetRTCaps</a>
</td>
<td align="left" width="63%">
Indicates whether the audio device is real-time (RT)-capable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudiodeviceendpoint-setbuffer">SetBuffer</a>
</td>
<td align="left" width="63%">
Sets the endpoint format and the size of the endpoint's buffer through which the audio data is streamed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudiodeviceendpoint-writeexclusivemodeparameterstosharedmemory">WriteExclusiveModeParametersToSharedMemory</a>
</td>
<td align="left" width="63%">
Creates and writes the exclusive-mode parameters to shared memory.

</td>
</tr>
</table> 


## -remarks



The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.



