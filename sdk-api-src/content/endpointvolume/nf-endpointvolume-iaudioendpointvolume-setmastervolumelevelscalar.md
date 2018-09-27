---
UID: NF:endpointvolume.IAudioEndpointVolume.SetMasterVolumeLevelScalar
title: IAudioEndpointVolume::SetMasterVolumeLevelScalar
author: windows-sdk-content
description: The SetMasterVolumeLevelScalar method sets the master volume level of the audio stream that enters or leaves the audio endpoint device. The volume level is expressed as a normalized, audio-tapered value in the range from 0.0 to 1.0.
old-location: coreaudio\iaudioendpointvolume_setmastervolumelevelscalar.htm
tech.root: CoreAudio
ms.assetid: d592c197-32fc-4a48-8f37-1cd140895c5e
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],SetMasterVolumeLevelScalar method, IAudioEndpointVolume.SetMasterVolumeLevelScalar, IAudioEndpointVolume::SetMasterVolumeLevelScalar, IAudioEndpointVolumeSetMasterVolumeLevelScalar, SetMasterVolumeLevelScalar, SetMasterVolumeLevelScalar method [Core Audio], SetMasterVolumeLevelScalar method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_setmastervolumelevelscalar, endpointvolume/IAudioEndpointVolume::SetMasterVolumeLevelScalar
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAudioEndpointVolume.SetMasterVolumeLevelScalar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointVolume::SetMasterVolumeLevelScalar


## -description



The <b>SetMasterVolumeLevelScalar</b> method sets the master volume level of the audio stream that enters or leaves the audio endpoint device. The volume level is expressed as a normalized, audio-tapered value in the range from 0.0 to 1.0.




## -parameters




### -param fLevel [in]

The new master volume level. The level is expressed as a normalized value in the range from 0.0 to 1.0.


### -param pguidEventContext [in]

Context value for the <a href="https://msdn.microsoft.com/a8ffad44-c621-4335-a312-16e7d6af2c18">IAudioEndpointVolumeCallback::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetMasterVolumeLevelScalar</b> call changes the volume level of the endpoint, all clients that have registered <a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback</a> interfaces with that endpoint will receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the volume-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the notification routine receives the context GUID value GUID_NULL.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>fLevel</i> is outside the range from 0.0 to 1.0.

</td>
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



The volume level is normalized to the range from 0.0 to 1.0, where 0.0 is the minimum volume level and 1.0 is the maximum level. Within this range, the relationship of the normalized volume level to the attenuation of signal amplitude is described by a nonlinear, audio-tapered curve. Note that the shape of the curve might change in future versions of Windows. For more information about audio-tapered curves, see <a href="https://msdn.microsoft.com/3b1adef5-40e9-4527-aa79-5a71f201fdfc">Audio-Tapered Volume Controls</a>.

The normalized volume levels that are passed to this method are suitable to represent the positions of volume controls in application windows and on-screen displays.

For a code example that calls <b>SetMasterVolumeLevelScalar</b>, see <a href="https://msdn.microsoft.com/667c3659-69ae-469d-9ae0-e32a189cbc71">Endpoint Volume Controls</a>.




## -see-also




<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>



<a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback Interface</a>



<a href="https://msdn.microsoft.com/a8ffad44-c621-4335-a312-16e7d6af2c18">IAudioEndpointVolumeCallback::OnNotify</a>
 

 

