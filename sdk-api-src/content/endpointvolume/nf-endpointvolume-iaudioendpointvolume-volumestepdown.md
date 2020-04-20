---
UID: NF:endpointvolume.IAudioEndpointVolume.VolumeStepDown
title: IAudioEndpointVolume::VolumeStepDown (endpointvolume.h)
description: The VolumeStepDown method decrements, by one step, the volume level of the audio stream that enters or leaves the audio endpoint device.helpviewer_keywords: ["IAudioEndpointVolume interface [Core Audio]","VolumeStepDown method","IAudioEndpointVolume.VolumeStepDown","IAudioEndpointVolume::VolumeStepDown","IAudioEndpointVolumeVolumeStepDown","VolumeStepDown","VolumeStepDown method [Core Audio]","VolumeStepDown method [Core Audio]","IAudioEndpointVolume interface","coreaudio.iaudioendpointvolume_volumestepdown","endpointvolume/IAudioEndpointVolume::VolumeStepDown"]
old-location: coreaudio\iaudioendpointvolume_volumestepdown.htm
tech.root: CoreAudio
ms.assetid: c334d780-784b-4fa3-bf4f-ea5d65459baf
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],VolumeStepDown method, IAudioEndpointVolume.VolumeStepDown, IAudioEndpointVolume::VolumeStepDown, IAudioEndpointVolumeVolumeStepDown, VolumeStepDown, VolumeStepDown method [Core Audio], VolumeStepDown method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_volumestepdown, endpointvolume/IAudioEndpointVolume::VolumeStepDown
f1_keywords:
- endpointvolume/IAudioEndpointVolume.VolumeStepDown
dev_langs:
- c++
req.header: endpointvolume.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Endpointvolume.h
api_name:
- IAudioEndpointVolume.VolumeStepDown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointVolume::VolumeStepDown


## -description



The <b>VolumeStepDown</b> method decrements, by one step, the volume level of the audio stream that enters or leaves the audio endpoint device.




## -parameters




### -param pguidEventContext [in]

Context value for the <a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>VolumeStepDown</b> call changes the volume level of the endpoint, all clients that have registered <a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback</a> interfaces with that endpoint will receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the volume-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.


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



To obtain the current volume step and the total number of steps in the volume range, call the <a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo">IAudioEndpointVolume::GetVolumeStepInfo</a> method.

If the volume level is already at the lowest step in the volume range, the call to <b>VolumeStepDown</b> has no effect and returns status code S_OK.

Successive intervals between adjacent steps do not necessarily represent uniform volume increments in either linear signal amplitude or decibels. In Windows Vista, <b>VolumeStepDown</b> defines the relationship of step index to volume level (signal amplitude) to be an audio-tapered curve. Note that the shape of the curve might change in future versions of Windows. For more information about audio-tapered curves, see <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/audio-tapered-volume-controls">Audio-Tapered Volume Controls</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumestepinfo">IAudioEndpointVolume::GetVolumeStepInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a>
 

 

