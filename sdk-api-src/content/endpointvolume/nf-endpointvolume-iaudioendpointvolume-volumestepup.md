---
UID: NF:endpointvolume.IAudioEndpointVolume.VolumeStepUp
title: IAudioEndpointVolume::VolumeStepUp
author: windows-sdk-content
description: The VolumeStepUp method increments, by one step, the volume level of the audio stream that enters or leaves the audio endpoint device.
old-location: coreaudio\iaudioendpointvolume_volumestepup.htm
old-project: CoreAudio
ms.assetid: 35ed44cd-ba91-4b6a-b528-0e22df389d31
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],VolumeStepUp method, IAudioEndpointVolume.VolumeStepUp, IAudioEndpointVolume::VolumeStepUp, IAudioEndpointVolumeVolumeStepUp, VolumeStepUp, VolumeStepUp method [Core Audio], VolumeStepUp method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_volumestepup, endpointvolume/IAudioEndpointVolume::VolumeStepUp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: endpointvolume.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: ProtType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolume.VolumeStepUp
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IAudioEndpointVolume::VolumeStepUp


## -description



The <b>VolumeStepUp</b> method increments, by one step, the volume level of the audio stream that enters or leaves the audio endpoint device.




## -parameters




### -param pguidEventContext [in]

Context value for the <a href="https://msdn.microsoft.com/a8ffad44-c621-4335-a312-16e7d6af2c18">IAudioEndpointVolumeCallback::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>VolumeStepUp</b> call changes the volume level of the endpoint, all clients that have registered <a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback</a> interfaces with that endpoint will receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the volume-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



To obtain the current volume step and the total number of steps in the volume range, call the <a href="https://msdn.microsoft.com/895f5dd1-73f5-464e-9498-b3832edf4dc7">IAudioEndpointVolume::GetVolumeStepInfo</a> method.

If the volume level is already at the highest step in the volume range, the call to <b>VolumeStepUp</b> has no effect and returns status code S_OK.

Successive intervals between adjacent steps do not necessarily represent uniform volume increments in either linear signal amplitude or decibels. In Windows Vista, <b>VolumeStepUp</b> defines the relationship of step index to volume level (signal amplitude) to be an audio-tapered curve. Note that the shape of the curve might change in future versions of Windows. For more information about audio-tapered curves, see <a href="https://msdn.microsoft.com/3b1adef5-40e9-4527-aa79-5a71f201fdfc">Audio-Tapered Volume Controls</a>.




## -see-also




<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>



<a href="https://msdn.microsoft.com/895f5dd1-73f5-464e-9498-b3832edf4dc7">IAudioEndpointVolume::GetVolumeStepInfo</a>



<a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback Interface</a>



<a href="https://msdn.microsoft.com/a8ffad44-c621-4335-a312-16e7d6af2c18">IAudioEndpointVolumeCallback::OnNotify</a>
 

 

