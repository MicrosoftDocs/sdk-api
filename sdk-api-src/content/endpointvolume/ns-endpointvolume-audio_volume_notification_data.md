---
UID: NS:endpointvolume.AUDIO_VOLUME_NOTIFICATION_DATA
title: AUDIO_VOLUME_NOTIFICATION_DATA (endpointvolume.h)
description: The AUDIO_VOLUME_NOTIFICATION_DATA structure describes a change in the volume level or muting state of an audio endpoint device.
helpviewer_keywords: ["*PAUDIO_VOLUME_NOTIFICATION_DATA","AUDIO_VOLUME_NOTIFICATION_DATA","AUDIO_VOLUME_NOTIFICATION_DATA structure [Core Audio]","AUDIO_VOLUME_NOTIFICATION_DATAStructure","PAUDIO_VOLUME_NOTIFICATION_DATA","PAUDIO_VOLUME_NOTIFICATION_DATA structure pointer [Core Audio]","coreaudio.audio_volume_notification_data","endpointvolume/AUDIO_VOLUME_NOTIFICATION_DATA","endpointvolume/PAUDIO_VOLUME_NOTIFICATION_DATA"]
old-location: coreaudio\audio_volume_notification_data.htm
tech.root: CoreAudio
ms.assetid: 8778eb32-bc37-4d21-a096-f932db3d7b3f
ms.date: 12/05/2018
ms.keywords: '*PAUDIO_VOLUME_NOTIFICATION_DATA, AUDIO_VOLUME_NOTIFICATION_DATA, AUDIO_VOLUME_NOTIFICATION_DATA structure [Core Audio], AUDIO_VOLUME_NOTIFICATION_DATAStructure, PAUDIO_VOLUME_NOTIFICATION_DATA, PAUDIO_VOLUME_NOTIFICATION_DATA structure pointer [Core Audio], coreaudio.audio_volume_notification_data, endpointvolume/AUDIO_VOLUME_NOTIFICATION_DATA, endpointvolume/PAUDIO_VOLUME_NOTIFICATION_DATA'
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
targetos: Windows
req.typenames: AUDIO_VOLUME_NOTIFICATION_DATA, *PAUDIO_VOLUME_NOTIFICATION_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AUDIO_VOLUME_NOTIFICATION_DATA
 - endpointvolume/AUDIO_VOLUME_NOTIFICATION_DATA
 - PAUDIO_VOLUME_NOTIFICATION_DATA
 - endpointvolume/PAUDIO_VOLUME_NOTIFICATION_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Endpointvolume.h
api_name:
 - AUDIO_VOLUME_NOTIFICATION_DATA
---

# AUDIO_VOLUME_NOTIFICATION_DATA structure


## -description

The <b>AUDIO_VOLUME_NOTIFICATION_DATA</b> structure describes a change in the volume level or muting state of an audio endpoint device.

## -struct-fields

### -field guidEventContext

Context value for the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a> method. This member is the value of the event-context GUID that was provided as an input parameter to the <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume</a> method call that changed the endpoint volume level or muting state. For more information, see Remarks.

### -field bMuted

Specifies whether the audio stream is currently muted. If <b>bMuted</b> is <b>TRUE</b>, the stream is muted. If <b>FALSE</b>, the stream is not muted.

### -field fMasterVolume

Specifies the current master volume level of the audio stream. The volume level is normalized to the range from 0.0 to 1.0, where 0.0 is the minimum volume level and 1.0 is the maximum level. Within this range, the relationship of the normalized volume level to the attenuation of signal amplitude is described by a nonlinear, audio-tapered curve. For more information about audio tapers, see <a href="/windows/desktop/CoreAudio/audio-tapered-volume-controls">Audio-Tapered Volume Controls</a>.

### -field nChannels

Specifies the number of channels in the audio stream, which is also the number of elements in the <b>afChannelVolumes</b> array. If the audio stream contains <i>n</i> channels, the channels are numbered from 0 to <i>n</i>-1. The volume level for a particular channel is contained in the array element whose index matches the channel number.

### -field afChannelVolumes

The first element in an array of channel volumes. This element contains the current volume level of channel 0 in the audio stream. If the audio stream contains more than one channel, the volume levels for the additional channels immediately follow the <b>AUDIO_VOLUME_NOTIFICATION_DATA</b> structure. The volume level for each channel is normalized to the range from 0.0 to 1.0, where 0.0 is the minimum volume level and 1.0 is the maximum level. Within this range, the relationship of the normalized volume level to the attenuation of signal amplitude is described by a nonlinear, audio-tapered curve.

## -remarks

This structure is used by the <b>IAudioEndpointVolumeCallback::OnNotify</b> method.

A client can register to be notified when the volume level or muting state of an endpoint device changes. The following methods can cause such a change:

<ul>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel">IAudioEndpointVolume::SetChannelVolumeLevel</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar">IAudioEndpointVolume::SetChannelVolumeLevelScalar</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel">IAudioEndpointVolume::SetMasterVolumeLevel</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar">IAudioEndpointVolume::SetMasterVolumeLevelScalar</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute">IAudioEndpointVolume::SetMute</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown">IAudioEndpointVolume::VolumeStepDown</a>
</li>
<li>
<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup">IAudioEndpointVolume::VolumeStepUp</a>
</li>
</ul>
When a call to one of these methods causes a volume-change event (that is, a change in the volume level or muting state), the method sends notifications to all clients that have registered to receive them. The method notifies a client by calling the client's <b>IAudioEndpointVolumeCallback::OnNotify</b> method. Through the <b>OnNotify</b> call, the client receives a pointer to an <b>AUDIO_VOLUME_NOTIFICATION_DATA</b> structure that describes the change.

Each of the methods in the preceding list accepts an input parameter named <i>pguidEventContext</i>, which is a pointer to an event-context GUID. Before sending notifications to clients, the method copies the event-context GUID pointed to by <i>pguidEventContext</i> into the <b>guidEventContext</b> member of the <b>AUDIO_VOLUME_NOTIFICATION_DATA</b> structure that it supplies to clients through their <b>OnNotify</b> methods. If <i>pguidEventContext</i> is <b>NULL</b>, the value of the <b>guidEventContext</b> member is set to GUID_NULL.

In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID from that call to discover whether it or another client is the source of the volume-change event.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-structures">Core Audio Structures</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel">IAudioEndpointVolume::SetChannelVolumeLevel</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar">IAudioEndpointVolume::SetChannelVolumeLevelScalar</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel">IAudioEndpointVolume::SetMasterVolumeLevel</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar">IAudioEndpointVolume::SetMasterVolumeLevelScalar</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute">IAudioEndpointVolume::SetMute</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown">IAudioEndpointVolume::VolumeStepDown</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup">IAudioEndpointVolume::VolumeStepUp</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a>