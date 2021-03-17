---
UID: NF:endpointvolume.IAudioEndpointVolume.SetChannelVolumeLevel
title: IAudioEndpointVolume::SetChannelVolumeLevel (endpointvolume.h)
description: The SetChannelVolumeLevel method sets the volume level, in decibels, of the specified channel of the audio stream that enters or leaves the audio endpoint device.
helpviewer_keywords: ["IAudioEndpointVolume interface [Core Audio]","SetChannelVolumeLevel method","IAudioEndpointVolume.SetChannelVolumeLevel","IAudioEndpointVolume::SetChannelVolumeLevel","IAudioEndpointVolumeSetChannelVolumeLevel","SetChannelVolumeLevel","SetChannelVolumeLevel method [Core Audio]","SetChannelVolumeLevel method [Core Audio]","IAudioEndpointVolume interface","coreaudio.iaudioendpointvolume_setchannelvolumelevel","endpointvolume/IAudioEndpointVolume::SetChannelVolumeLevel"]
old-location: coreaudio\iaudioendpointvolume_setchannelvolumelevel.htm
tech.root: CoreAudio
ms.assetid: 51f3b4dd-be9d-4b83-8605-a9962c6709a3
ms.date: 12/05/2018
ms.keywords: IAudioEndpointVolume interface [Core Audio],SetChannelVolumeLevel method, IAudioEndpointVolume.SetChannelVolumeLevel, IAudioEndpointVolume::SetChannelVolumeLevel, IAudioEndpointVolumeSetChannelVolumeLevel, SetChannelVolumeLevel, SetChannelVolumeLevel method [Core Audio], SetChannelVolumeLevel method [Core Audio],IAudioEndpointVolume interface, coreaudio.iaudioendpointvolume_setchannelvolumelevel, endpointvolume/IAudioEndpointVolume::SetChannelVolumeLevel
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
 - IAudioEndpointVolume::SetChannelVolumeLevel
 - endpointvolume/IAudioEndpointVolume::SetChannelVolumeLevel
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
 - IAudioEndpointVolume.SetChannelVolumeLevel
---

# IAudioEndpointVolume::SetChannelVolumeLevel


## -description

The <b>SetChannelVolumeLevel</b> method sets the volume level, in decibels, of the specified channel of the audio stream that enters or leaves the audio endpoint device.

## -parameters

### -param nChannel [in]

The channel number. If the audio stream contains <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. To obtain the number of channels, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelcount">IAudioEndpointVolume::GetChannelCount</a> method.

### -param fLevelDB [in]

The new volume level in decibels. To obtain the range and granularity of the volume levels that can be set by this method, call the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange">IAudioEndpointVolume::GetVolumeRange</a> method.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetChannelVolumeLevel</b> call changes the volume level of the endpoint, all clients that have registered <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback</a> interfaces with that endpoint will receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the volume-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the notification routine receives the context GUID value GUID_NULL.

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
Parameter <i>nChannel</i> is greater than or equal to the number of channels in the stream; or parameter <i>fLevelDB</i> lies outside of the volume range supported by the device.

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

If volume level <i>fLevelDB</i> falls outside of the volume range reported by the <b>IAudioEndpointVolume::GetVolumeRange</b> method, the <b>SetChannelVolumeLevel</b> call fails and returns error code E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getchannelcount">IAudioEndpointVolume::GetChannelCount</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolume-getvolumerange">IAudioEndpointVolume::GetVolumeRange</a>



<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback">IAudioEndpointVolumeCallback Interface</a>



<a href="/windows/desktop/api/endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify">IAudioEndpointVolumeCallback::OnNotify</a>