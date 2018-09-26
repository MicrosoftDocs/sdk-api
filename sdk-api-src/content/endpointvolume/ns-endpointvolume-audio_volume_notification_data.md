---
UID: NS:endpointvolume.AUDIO_VOLUME_NOTIFICATION_DATA
title: AUDIO_VOLUME_NOTIFICATION_DATA
author: windows-sdk-content
description: The AUDIO_VOLUME_NOTIFICATION_DATA structure describes a change in the volume level or muting state of an audio endpoint device.
old-location: coreaudio\audio_volume_notification_data.htm
tech.root: CoreAudio
ms.assetid: 8778eb32-bc37-4d21-a096-f932db3d7b3f
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: "*PAUDIO_VOLUME_NOTIFICATION_DATA, AUDIO_VOLUME_NOTIFICATION_DATA, AUDIO_VOLUME_NOTIFICATION_DATA structure [Core Audio], AUDIO_VOLUME_NOTIFICATION_DATAStructure, PAUDIO_VOLUME_NOTIFICATION_DATA, PAUDIO_VOLUME_NOTIFICATION_DATA structure pointer [Core Audio], coreaudio.audio_volume_notification_data, endpointvolume/AUDIO_VOLUME_NOTIFICATION_DATA, endpointvolume/PAUDIO_VOLUME_NOTIFICATION_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - HeaderDef
api_location:
 - Endpointvolume.h
api_name:
 - AUDIO_VOLUME_NOTIFICATION_DATA
product: Windows
targetos: Windows
req.typenames: AUDIO_VOLUME_NOTIFICATION_DATA, *PAUDIO_VOLUME_NOTIFICATION_DATA
req.redist: 
---

# AUDIO_VOLUME_NOTIFICATION_DATA structure


## -description



The <b>AUDIO_VOLUME_NOTIFICATION_DATA</b> structure describes a change in the volume level or muting state of an audio endpoint device.




## -struct-fields




### -field guidEventContext

Context value for the <a href="https://msdn.microsoft.com/a8ffad44-c621-4335-a312-16e7d6af2c18">IAudioEndpointVolumeCallback::OnNotify</a> method. This member is the value of the event-context GUID that was provided as an input parameter to the <a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume</a> method call that changed the endpoint volume level or muting state. For more information, see Remarks.


### -field bMuted

Specifies whether the audio stream is currently muted. If <b>bMuted</b> is <b>TRUE</b>, the stream is muted. If <b>FALSE</b>, the stream is not muted.


### -field fMasterVolume

Specifies the current master volume level of the audio stream. The volume level is normalized to the range from 0.0 to 1.0, where 0.0 is the minimum volume level and 1.0 is the maximum level. Within this range, the relationship of the normalized volume level to the attenuation of signal amplitude is described by a nonlinear, audio-tapered curve. For more information about audio tapers, see <a href="https://msdn.microsoft.com/3b1adef5-40e9-4527-aa79-5a71f201fdfc">Audio-Tapered Volume Controls</a>.


### -field nChannels

Specifies the number of channels in the audio stream, which is also the number of elements in the <b>afChannelVolumes</b> array. If the audio stream contains <i>n</i> channels, the channels are numbered from 0 to <i>n</i>-1. The volume level for a particular channel is contained in the array element whose index matches the channel number.


### -field afChannelVolumes

The first element in an array of channel volumes. This element contains the current volume level of channel 0 in the audio stream. If the audio stream contains more than one channel, the volume levels for the additional channels immediately follow the <b>AUDIO_VOLUME_NOTIFICATION_DATA</b> structure. The volume level for each channel is normalized to the range from 0.0 to 1.0, where 0.0 is the minimum volume level and 1.0 is the maximum level. Within this range, the relationship of the normalized volume level to the attenuation of signal amplitude is described by a nonlinear, audio-tapered curve.


## -remarks



This structure is used by the <b>IAudioEndpointVolumeCallback::OnNotify</b> method.

A client can register to be notified when the volume level or muting state of an endpoint device changes. The following methods can cause such a change:

<ul>
<li>
<a href="https://msdn.microsoft.com/51f3b4dd-be9d-4b83-8605-a9962c6709a3">IAudioEndpointVolume::SetChannelVolumeLevel</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2e1f0d1c-060f-45b7-9194-591e45668b52">IAudioEndpointVolume::SetChannelVolumeLevelScalar</a>
</li>
<li>
<a href="https://msdn.microsoft.com/776d7667-f48b-44c0-9441-177b86b52da9">IAudioEndpointVolume::SetMasterVolumeLevel</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d592c197-32fc-4a48-8f37-1cd140895c5e">IAudioEndpointVolume::SetMasterVolumeLevelScalar</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a0ab4fef-8333-4f21-ae8e-74285788ae0e">IAudioEndpointVolume::SetMute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c334d780-784b-4fa3-bf4f-ea5d65459baf">IAudioEndpointVolume::VolumeStepDown</a>
</li>
<li>
<a href="https://msdn.microsoft.com/35ed44cd-ba91-4b6a-b528-0e22df389d31">IAudioEndpointVolume::VolumeStepUp</a>
</li>
</ul>
When a call to one of these methods causes a volume-change event (that is, a change in the volume level or muting state), the method sends notifications to all clients that have registered to receive them. The method notifies a client by calling the client's <b>IAudioEndpointVolumeCallback::OnNotify</b> method. Through the <b>OnNotify</b> call, the client receives a pointer to an <b>AUDIO_VOLUME_NOTIFICATION_DATA</b> structure that describes the change.

Each of the methods in the preceding list accepts an input parameter named <i>pguidEventContext</i>, which is a pointer to an event-context GUID. Before sending notifications to clients, the method copies the event-context GUID pointed to by <i>pguidEventContext</i> into the <b>guidEventContext</b> member of the <b>AUDIO_VOLUME_NOTIFICATION_DATA</b> structure that it supplies to clients through their <b>OnNotify</b> methods. If <i>pguidEventContext</i> is <b>NULL</b>, the value of the <b>guidEventContext</b> member is set to GUID_NULL.

In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID from that call to discover whether it or another client is the source of the volume-change event. 




## -see-also




<a href="https://msdn.microsoft.com/92585cd4-baa9-4f75-816e-b83f5badad37">Core Audio Structures</a>



<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>



<a href="https://msdn.microsoft.com/51f3b4dd-be9d-4b83-8605-a9962c6709a3">IAudioEndpointVolume::SetChannelVolumeLevel</a>



<a href="https://msdn.microsoft.com/2e1f0d1c-060f-45b7-9194-591e45668b52">IAudioEndpointVolume::SetChannelVolumeLevelScalar</a>



<a href="https://msdn.microsoft.com/776d7667-f48b-44c0-9441-177b86b52da9">IAudioEndpointVolume::SetMasterVolumeLevel</a>



<a href="https://msdn.microsoft.com/d592c197-32fc-4a48-8f37-1cd140895c5e">IAudioEndpointVolume::SetMasterVolumeLevelScalar</a>



<a href="https://msdn.microsoft.com/a0ab4fef-8333-4f21-ae8e-74285788ae0e">IAudioEndpointVolume::SetMute</a>



<a href="https://msdn.microsoft.com/c334d780-784b-4fa3-bf4f-ea5d65459baf">IAudioEndpointVolume::VolumeStepDown</a>



<a href="https://msdn.microsoft.com/35ed44cd-ba91-4b6a-b528-0e22df389d31">IAudioEndpointVolume::VolumeStepUp</a>



<a href="https://msdn.microsoft.com/0b631d1b-f89c-4789-a09c-875b24a48a89">IAudioEndpointVolumeCallback Interface</a>



<a href="https://msdn.microsoft.com/a8ffad44-c621-4335-a312-16e7d6af2c18">IAudioEndpointVolumeCallback::OnNotify</a>
 

 

