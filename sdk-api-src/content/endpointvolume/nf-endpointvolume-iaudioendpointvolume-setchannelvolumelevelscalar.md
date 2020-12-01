---
UID: NF:endpointvolume.IAudioEndpointVolume.SetChannelVolumeLevelScalar
title: IAudioEndpointVolume::SetChannelVolumeLevelScalar (endpointvolume.h)
description: The SetChannelVolumeLevelScalar method sets the normalized, audio-tapered volume level of the specified channel in the audio stream that enters or leaves the audio endpoint device.
helpviewer_keywords: ["IAudioEndpointVolume interface [Core Audio]","SetChannelVolumeLevelScalar method","IAudioEndpointVolume.SetChannelVolumeLevelScalar","IAudioEndpointVolume::SetChannelVolumeLevelScalar","IAudioEndpointVolumeSetChannelVolumeLevelScalar","SetChannelVolumeLevelScalar","SetChannelVolumeLevelScalar method [Core Audio]","SetChannelVolumeLevelScalar method [Core Audio]","IAudioEndpointVolume interface","coreaudio.iaudioendpointvolume_setchannelvolumelevelscalar","endpointvolume/IAudioEndpointVolume::SetChannelVolumeLevelScalar"]
old-location: coreaudio\iaudioendpointvolume_setchannelvolumelevelscalar.htm
tech.root: CoreAudio
ms.assetid: 2e1f0d1c-060f-45b7-9194-591e45668b52
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],SetChannelVolumeLevelScalar method, IAudioEndpointVolume.SetChannelVolumeLevelScalar, IAudioEndpointVolume::SetChannelVolumeLevelScalar, IAudioEndpointVolumeSetChannelVolumeLevelScalar, SetChannelVolumeLevelScalar, SetChannelVolumeLevelScalar method [Core Audio], SetChannelVolumeLevelScalar method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_setchannelvolumelevelscalar, endpointvolume/IAudioEndpointVolume::SetChannelVolumeLevelScalar
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioEndpointVolume::SetChannelVolumeLevelScalar
 - endpointvolume/IAudioEndpointVolume::SetChannelVolumeLevelScalar
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioEndpointVolume.SetChannelVolumeLevelScalar
---

# IAudioEndpointVolume::SetChannelVolumeLevelScalar


## -description

The <b>SetChannelVolumeLevelScalar</b> method sets the normalized, audio-tapered volume level of the specified channel in the audio stream that enters or leaves the audio endpoint device.

## -parameters

### -param nChannel [in]

The channel number. If the audio stream contains <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. To obtain the number of channels, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelcount">IAudioEndpointVolume::GetChannelCount</a> method.

### -param fLevel [in]

The volume level. The volume level is expressed as a normalized value in the range from 0.0 to 1.0.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetChannelVolumeLevelScalar</b> call changes the volume level of the endpoint, all clients that have registered <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback</a> interfaces with that endpoint will receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the volume-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the notification routine receives the context GUID value GUID_NULL.

## -returns

If the method succeeds, it returns S_OK. If the method fails, possible return codes include, but are not limited to, the values shown in the following table.

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
Parameter <i>nChannel</i> is greater than or equal to the number of channels in the stream; or parameter <i>fLevel</i> is outside the range from 0.0 to 1.0.

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

The volume level is normalized to the range from 0.0 to 1.0, where 0.0 is the minimum volume level and 1.0 is the maximum level. Within this range, the relationship of the normalized volume level to the attenuation of signal amplitude is described by a nonlinear, audio-tapered curve. Note that the shape of the curve might change in future versions of Windows. For more information about audio-tapered curves, see <a href="/windows/desktop/CoreAudio/audio-tapered-volume-controls">Audio-Tapered Volume Controls</a>.

The normalized volume levels that are passed to this method are suitable to represent the positions of volume controls in application windows and on-screen displays.

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelcount">IAudioEndpointVolume::GetChannelCount</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a>