---
UID: NN:audioengineendpoint.IAudioDeviceEndpoint
title: IAudioDeviceEndpoint
author: windows-sdk-content
description: Initializes a device endpoint object and gets the capabilities of the device that it represents.
old-location: termserv\iaudiodeviceendpoint.htm
old-project: termserv
ms.assetid: 3112bc7e-e138-4b42-8f82-61fdf19f7e94
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: IAudioDeviceEndpoint, IAudioDeviceEndpoint interface [Remote Desktop Services], IAudioDeviceEndpoint interface [Remote Desktop Services],described, audioengineendpoint/IAudioDeviceEndpoint, termserv.iaudiodeviceendpoint
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
tech.root: 
req.typenames: AE_POSITION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioDeviceEndpoint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioDeviceEndpoint interface


## -description


Initializes a device endpoint object and gets the capabilities of the device that it represents.


        A <i>device endpoint</i> abstracts an audio device. The device can be a rendering device such as a speaker or a capture  device such as a microphone. A device endpoint must implement the <b>IAudioDeviceEndpoint</b> interface.
      

To a get a reference to the <b>IAudioDeviceEndpoint</b> interface of the device, the audio engine calls <b>QueryInterface</b> on the audio endpoint (<a href="https://msdn.microsoft.com/f9638dea-f61d-45f6-b91d-72e4fc1b4a92">IAudioInputEndpointRT</a> or <a href="https://msdn.microsoft.com/b881b2f9-ffe9-46ff-94aa-eef0af172a3e">IAudioOutputEndpointRT</a>) for the device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioDeviceEndpoint</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAudioDeviceEndpoint</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/56ed44ee-44dd-4a56-a4cc-2983d4802773">GetEventDrivenCapable</a>
</td>
<td align="left" width="63%">
Indicates whether the audio endpoint can be event driven.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba8aa8c2-8d62-477a-b5c0-338c989c57a6">GetRTCaps</a>
</td>
<td align="left" width="63%">
Indicates whether the audio device is real-time (RT)-capable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983423">SetBuffer</a>
</td>
<td align="left" width="63%">
Sets the endpoint format and the size of the endpoint's buffer through which the audio data is streamed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0484432a-4bbe-4892-8888-f11d6384d387">WriteExclusiveModeParametersToSharedMemory</a>
</td>
<td align="left" width="63%">
Creates and writes the exclusive-mode parameters to shared memory.

</td>
</tr>
</table> 


## -remarks



The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.



