---
UID: NF:audioclient.ISimpleAudioVolume.SetMute
title: ISimpleAudioVolume::SetMute (audioclient.h)
description: The SetMute method sets the muting state for the audio session.
helpviewer_keywords: ["ISimpleAudioVolume interface [Core Audio]","SetMute method","ISimpleAudioVolume.SetMute","ISimpleAudioVolume::SetMute","ISimpleAudioVolumeSetMute","SetMute","SetMute method [Core Audio]","SetMute method [Core Audio]","ISimpleAudioVolume interface","audioclient/ISimpleAudioVolume::SetMute","coreaudio.isimpleaudiovolume_setmute"]
old-location: coreaudio\isimpleaudiovolume_setmute.htm
tech.root: CoreAudio
ms.assetid: 64fc7146-8d4b-429c-bf35-c43e31a41af8
ms.date: 12/05/2018
ms.keywords: ISimpleAudioVolume interface [Core Audio],SetMute method, ISimpleAudioVolume.SetMute, ISimpleAudioVolume::SetMute, ISimpleAudioVolumeSetMute, SetMute, SetMute method [Core Audio], SetMute method [Core Audio],ISimpleAudioVolume interface, audioclient/ISimpleAudioVolume::SetMute, coreaudio.isimpleaudiovolume_setmute
req.header: audioclient.h
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
 - ISimpleAudioVolume::SetMute
 - audioclient/ISimpleAudioVolume::SetMute
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
 - ISimpleAudioVolume.SetMute
---

# ISimpleAudioVolume::SetMute


## -description

The <b>SetMute</b> method sets the muting state for the audio session.

## -parameters

### -param bMute [in]

The new muting state. <b>TRUE</b> enables muting. <b>FALSE</b> disables muting.

### -param EventContext [in]

Pointer to the event-context GUID. If a call to this method generates a volume-change event, the session manager sends notifications to all clients that have registered <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interfaces with the session manager. The session manager includes the <i>EventContext</i> pointer value with each notification. Upon receiving a notification, a client can determine whether it or another client is the source of the event by inspecting the <i>EventContext</i> value. This scheme depends on the client selecting a value for this parameter that is unique among all clients in the session. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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

This method generates a volume-change event only if the method call changes the muting state of the session from disabled to enabled, or from enabled to disabled. For example, if muting is enabled when the call occurs, and the call enables muting, no event is generated.

This method applies the same muting state to all channels in the audio session. The endpoint device always applies muting uniformly across all the channels in the session. There are no <a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume</a> methods for setting the muting states of individual channels.

The client can get the muting state of the audio session by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-getmute">SimpleAudioVolume::GetMute</a> method.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-getmute">ISimpleAudioVolume::GetMute</a>