---
UID: NF:audioclient.IChannelAudioVolume.SetChannelVolume
title: IChannelAudioVolume::SetChannelVolume (audioclient.h)
description: The SetChannelVolume method sets the volume level for the specified channel in the audio session.
helpviewer_keywords: ["IChannelAudioVolume interface [Core Audio]","SetChannelVolume method","IChannelAudioVolume.SetChannelVolume","IChannelAudioVolume::SetChannelVolume","IChannelAudioVolumeSetChannelVolume","SetChannelVolume","SetChannelVolume method [Core Audio]","SetChannelVolume method [Core Audio]","IChannelAudioVolume interface","audioclient/IChannelAudioVolume::SetChannelVolume","coreaudio.ichannelaudiovolume_setchannelvolume"]
old-location: coreaudio\ichannelaudiovolume_setchannelvolume.htm
tech.root: CoreAudio
ms.assetid: b7baeebf-01d3-4dec-a674-73a84bbf7a66
ms.date: 12/05/2018
ms.keywords: IChannelAudioVolume interface [Core Audio],SetChannelVolume method, IChannelAudioVolume.SetChannelVolume, IChannelAudioVolume::SetChannelVolume, IChannelAudioVolumeSetChannelVolume, SetChannelVolume, SetChannelVolume method [Core Audio], SetChannelVolume method [Core Audio],IChannelAudioVolume interface, audioclient/IChannelAudioVolume::SetChannelVolume, coreaudio.ichannelaudiovolume_setchannelvolume
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
 - IChannelAudioVolume::SetChannelVolume
 - audioclient/IChannelAudioVolume::SetChannelVolume
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
 - IChannelAudioVolume.SetChannelVolume
---

# IChannelAudioVolume::SetChannelVolume


## -description

The <b>SetChannelVolume</b> method sets the volume level for the specified channel in the audio session.

## -parameters

### -param dwIndex [in]

The channel number. If the stream format for the audio session has <i>N</i> channels, the channels are numbered from 0 to <i>N</i>– 1. To get the number of channels, call the <a href="/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-getchannelcount">IChannelAudioVolume::GetChannelCount</a> method.

### -param fLevel [in]

The volume level for the channel. Valid volume levels are in the range 0.0 to 1.0.

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
Parameter <i>dwIndex</i> is set to an invalid channel number, or parameter <i>fLevel</i> is not in the range 0.0 to 1.0.

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

This method, if it succeeds, generates a channel-volume-change event regardless of whether the new channel volume level differs in value from the previous channel volume level.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-getchannelcount">IChannelAudioVolume::GetChannelCount</a>