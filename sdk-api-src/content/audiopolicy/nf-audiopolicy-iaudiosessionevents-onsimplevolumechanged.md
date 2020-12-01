---
UID: NF:audiopolicy.IAudioSessionEvents.OnSimpleVolumeChanged
title: IAudioSessionEvents::OnSimpleVolumeChanged (audiopolicy.h)
description: The OnSimpleVolumeChanged method notifies the client that the volume level or muting state of the audio session has changed.
helpviewer_keywords: ["IAudioSessionEvents interface [Core Audio]","OnSimpleVolumeChanged method","IAudioSessionEvents.OnSimpleVolumeChanged","IAudioSessionEvents::OnSimpleVolumeChanged","IAudioSessionEventsOnSimpleVolumeChanged","OnSimpleVolumeChanged","OnSimpleVolumeChanged method [Core Audio]","OnSimpleVolumeChanged method [Core Audio]","IAudioSessionEvents interface","audiopolicy/IAudioSessionEvents::OnSimpleVolumeChanged","coreaudio.iaudiosessionevents_onsimplevolumechanged"]
old-location: coreaudio\iaudiosessionevents_onsimplevolumechanged.htm
tech.root: CoreAudio
ms.assetid: e60e8996-3c01-4458-88f2-cd6cb118bd76
ms.date: 12/05/2018
ms.keywords: IAudioSessionEvents interface [Core Audio],OnSimpleVolumeChanged method, IAudioSessionEvents.OnSimpleVolumeChanged, IAudioSessionEvents::OnSimpleVolumeChanged, IAudioSessionEventsOnSimpleVolumeChanged, OnSimpleVolumeChanged, OnSimpleVolumeChanged method [Core Audio], OnSimpleVolumeChanged method [Core Audio],IAudioSessionEvents interface, audiopolicy/IAudioSessionEvents::OnSimpleVolumeChanged, coreaudio.iaudiosessionevents_onsimplevolumechanged
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
 - IAudioSessionEvents::OnSimpleVolumeChanged
 - audiopolicy/IAudioSessionEvents::OnSimpleVolumeChanged
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
 - IAudioSessionEvents.OnSimpleVolumeChanged
---

# IAudioSessionEvents::OnSimpleVolumeChanged


## -description

The <b>OnSimpleVolumeChanged</b> method notifies the client that the volume level or muting state of the audio session has changed.

## -parameters

### -param NewVolume [in]

The new volume level for the audio session. This parameter is a value in the range 0.0 to 1.0, where 0.0 is silence and 1.0 is full volume (no attenuation).

### -param NewMute [in]

The new muting state. If <b>TRUE</b>, muting is enabled. If <b>FALSE</b>, muting is disabled.

### -param EventContext [in]

The event context value. This is the same value that the caller passed to <a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume">ISimpleAudioVolume::SetMasterVolume</a> or <a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-setmute">ISimpleAudioVolume::SetMute</a> in the call that changed the volume level or muting state of the session. For more information, see Remarks.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The session manager calls this method each time a call to the <a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume">ISimpleAudioVolume::SetMasterVolume</a> or <a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-setmute">ISimpleAudioVolume::SetMute</a> method changes the volume level or muting state of the session.

The <i>EventContext</i> parameter provides a means for a client to distinguish between a volume or mute change that it initiated and one that some other client initiated. When calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume">ISimpleAudioVolume::SetMasterVolume</a> or <a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-setmute">ISimpleAudioVolume::SetMute</a> method, a client passes in an <i>EventContext</i> parameter value that its implementation of the <b>OnSimpleVolumeChanged</b> method can recognize.

For a code example that implements the methods in the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interface, see <a href="/windows/desktop/CoreAudio/audio-session-events">Audio Session Events</a>.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume">ISimpleAudioVolume::SetMasterVolume</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-isimpleaudiovolume-setmute">ISimpleAudioVolume::SetMute</a>