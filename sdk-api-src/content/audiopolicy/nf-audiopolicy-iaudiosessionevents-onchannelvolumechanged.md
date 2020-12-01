---
UID: NF:audiopolicy.IAudioSessionEvents.OnChannelVolumeChanged
title: IAudioSessionEvents::OnChannelVolumeChanged (audiopolicy.h)
description: The OnChannelVolumeChanged method notifies the client that the volume level of an audio channel in the session submix has changed.
helpviewer_keywords: ["IAudioSessionEvents interface [Core Audio]","OnChannelVolumeChanged method","IAudioSessionEvents.OnChannelVolumeChanged","IAudioSessionEvents::OnChannelVolumeChanged","IAudioSessionEventsOnChannelVolumeChanged","OnChannelVolumeChanged","OnChannelVolumeChanged method [Core Audio]","OnChannelVolumeChanged method [Core Audio]","IAudioSessionEvents interface","audiopolicy/IAudioSessionEvents::OnChannelVolumeChanged","coreaudio.iaudiosessionevents_onchannelvolumechanged"]
old-location: coreaudio\iaudiosessionevents_onchannelvolumechanged.htm
tech.root: CoreAudio
ms.assetid: cdd3ec9b-cf72-4c2e-b874-60370d41447d
ms.date: 12/05/2018
ms.keywords: IAudioSessionEvents interface [Core Audio],OnChannelVolumeChanged method, IAudioSessionEvents.OnChannelVolumeChanged, IAudioSessionEvents::OnChannelVolumeChanged, IAudioSessionEventsOnChannelVolumeChanged, OnChannelVolumeChanged, OnChannelVolumeChanged method [Core Audio], OnChannelVolumeChanged method [Core Audio],IAudioSessionEvents interface, audiopolicy/IAudioSessionEvents::OnChannelVolumeChanged, coreaudio.iaudiosessionevents_onchannelvolumechanged
req.header: audiopolicy.h
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
 - IAudioSessionEvents::OnChannelVolumeChanged
 - audiopolicy/IAudioSessionEvents::OnChannelVolumeChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audiopolicy.h
api_name:
 - IAudioSessionEvents.OnChannelVolumeChanged
---

# IAudioSessionEvents::OnChannelVolumeChanged


## -description

The <b>OnChannelVolumeChanged</b> method notifies the client that the volume level of an audio channel in the session submix has changed.

## -parameters

### -param ChannelCount [in]

The channel count. This parameter specifies the number of audio channels in the session submix.

### -param NewChannelVolumeArray [in]

Pointer to an array of volume levels. Each element is a value of type <b>float</b> that specifies the volume level for a particular channel. Each volume level is a value in the range 0.0 to 1.0, where 0.0 is silence and 1.0 is full volume (no attenuation). The number of elements in the array is specified by the <i>ChannelCount</i> parameter. If an audio stream contains <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. The array element whose index matches the channel number, contains the volume level for that channel. Assume that the array remains valid only for the duration of the call.

### -param ChangedChannel [in]

The number of the channel whose volume level changed. Use this value as an index into the <i>NewChannelVolumeArray</i> array. If the session submix contains <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. If more than one channel might have changed (for example, as a result of a call to the <a href="/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-setallvolumes">IChannelAudioVolume::SetAllVolumes</a> method), the value of <i>ChangedChannel</i> is (<b>DWORD</b>)(–1).

### -param EventContext [in]

The event context value. This is the same value that the caller passed to the <a href="/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-setchannelvolume">IChannelAudioVolume::SetChannelVolume</a> or <b>IChannelAudioVolume::SetAllVolumes</b> method in the call that initiated the change in volume level of the channel. For more information, see Remarks.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The session manager calls this method each time a call to the <b>IChannelAudioVolume::SetChannelVolume</b> or <b>IChannelAudioVolume::SetAllVolumes</b> method successfully updates the volume level of one or more channels in the session submix. Note that the <b>OnChannelVolumeChanged</b> call occurs regardless of whether the new channel volume level or levels differ in value from the previous channel volume level or levels.

The <i>EventContext</i> parameter provides a means for a client to distinguish between a channel-volume change that it initiated and one that some other client initiated. When calling the <b>IChannelAudioVolume::SetChannelVolume</b> or <b>IChannelAudioVolume::SetAllVolumes</b> method, a client passes in an <i>EventContext</i> parameter value that its implementation of the <b>OnChannelVolumeChanged</b> method can recognize.

For a code example that implements the methods in the <b>IAudioSessionEvents</b> interface, see <a href="/windows/desktop/CoreAudio/audio-session-events">Audio Session Events</a>.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-setallvolumes">IChannelAudioVolume::SetAllVolumes</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-ichannelaudiovolume-setchannelvolume">IChannelAudioVolume::SetChannelVolume</a>