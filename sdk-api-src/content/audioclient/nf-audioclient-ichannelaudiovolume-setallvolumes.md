---
UID: NF:audioclient.IChannelAudioVolume.SetAllVolumes
title: IChannelAudioVolume::SetAllVolumes (audioclient.h)
description: The SetAllVolumes method sets the individual volume levels for all the channels in the audio session.
helpviewer_keywords: ["IChannelAudioVolume interface [Core Audio]","SetAllVolumes method","IChannelAudioVolume.SetAllVolumes","IChannelAudioVolume::SetAllVolumes","IChannelAudioVolumeSetAllVolumes","SetAllVolumes","SetAllVolumes method [Core Audio]","SetAllVolumes method [Core Audio]","IChannelAudioVolume interface","audioclient/IChannelAudioVolume::SetAllVolumes","coreaudio.ichannelaudiovolume_setallvolumes"]
old-location: coreaudio\ichannelaudiovolume_setallvolumes.htm
tech.root: CoreAudio
ms.assetid: 9081e814-d0b2-4b0e-9e4c-3590058e7196
ms.date: 12/05/2018
ms.keywords: IChannelAudioVolume interface [Core Audio],SetAllVolumes method, IChannelAudioVolume.SetAllVolumes, IChannelAudioVolume::SetAllVolumes, IChannelAudioVolumeSetAllVolumes, SetAllVolumes, SetAllVolumes method [Core Audio], SetAllVolumes method [Core Audio],IChannelAudioVolume interface, audioclient/IChannelAudioVolume::SetAllVolumes, coreaudio.ichannelaudiovolume_setallvolumes
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IChannelAudioVolume::SetAllVolumes
 - audioclient/IChannelAudioVolume::SetAllVolumes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IChannelAudioVolume.SetAllVolumes
---

# IChannelAudioVolume::SetAllVolumes


## -description

The <b>SetAllVolumes</b> method sets the individual volume levels for all the channels in the audio session.

## -parameters

### -param dwCount [in]

The number of elements in the <i>pfVolumes</i> array. This parameter must equal the number of channels in the stream format for the audio session. To get the number of channels, call the <a href="/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-getchannelcount">IChannelAudioVolume::GetChannelCount</a> method.

### -param pfVolumes [in]

Pointer to an array of volume levels for the channels in the audio session. The number of elements in the <i>pfVolumes</i> array is specified by the <i>dwCount</i> parameter. The caller writes the volume level for each channel to the array element whose index matches the channel number. If the stream format for the audio session has <i>N</i> channels, the channels are numbered from 0 to <i>N</i>– 1. Valid volume levels are in the range 0.0 to 1.0.

### -param EventContext [in]

Pointer to the event-context GUID. If a call to this method generates a channel-volume-change event, the session manager sends notifications to all clients that have registered <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interfaces with the session manager. The session manager includes the <i>EventContext</i> pointer value with each notification. Upon receiving a notification, a client can determine whether it or another client is the source of the event by inspecting the <i>EventContext</i> value. This scheme depends on the client selecting a value for this parameter that is unique among all clients in the session. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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
Parameter <i>dwCount</i> does not equal the number of channels in the stream format for the audio session, or the value of a <i>pfVolumes</i> array element is not in the range 0.0 to 1.0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pfVolumes</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>

## -remarks

This method, if it succeeds, generates a channel-volume-change event regardless of whether any of the new channel volume levels differ in value from the previous channel volume levels.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-getchannelcount">IChannelAudioVolume::GetChannelCount</a>