---
UID: NN:audioclient.IChannelAudioVolume
title: IChannelAudioVolume (audioclient.h)
description: The IChannelAudioVolume interface enables a client to control and monitor the volume levels for all of the channels in the audio session that the stream belongs to.
helpviewer_keywords: ["IChannelAudioVolume","IChannelAudioVolume interface [Core Audio]","IChannelAudioVolume interface [Core Audio]","described","audioclient/IChannelAudioVolume","coreaudio.ichannelaudiovolume"]
old-location: coreaudio\ichannelaudiovolume.htm
tech.root: CoreAudio
ms.assetid: 0d0a20dc-5e5a-49a7-adc9-20aacb88368a
ms.date: 12/05/2018
ms.keywords: IChannelAudioVolume, IChannelAudioVolume interface [Core Audio], IChannelAudioVolume interface [Core Audio],described, audioclient/IChannelAudioVolume, coreaudio.ichannelaudiovolume
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
 - IChannelAudioVolume
 - audioclient/IChannelAudioVolume
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
 - IChannelAudioVolume
---

# IChannelAudioVolume interface


## -description

The <b>IChannelAudioVolume</b> interface enables a client to control and monitor the volume levels for all of the channels in the <a href="/windows/desktop/CoreAudio/audio-sessions">audio session</a> that the stream belongs to. This is the session that the client assigned the stream to during the call to the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method. The client obtains a reference to the <b>IChannelAudioVolume</b> interface on a stream object by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to REFIID IID_IChannelAudioVolume.

The effective volume level of any channel in the session submix, as heard at the speakers, is the product of the following four volume-level factors:

<ul>
<li>The per-channel volume levels of the streams in the session, which clients can control through the methods in the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiostreamvolume">IAudioStreamVolume</a> interface.</li>
<li>The per-channel volume level of the session, which clients can control through the methods in the <b>IChannelAudioVolume</b> interface.</li>
<li>The master volume level of the session, which clients can control through the methods in the <a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume</a> interface.</li>
<li>The policy-based volume level of the session, which the system dynamically assigns to the session as the global mix changes.</li>
</ul>
Each of the four volume-level factors in the preceding list is a value in the range 0.0 to 1.0, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation). The effective volume level is also a value in the range 0.0 to 1.0.

Typical audio applications do not modify the volume levels of sessions. Instead, they rely on users to set these volume levels through the Sndvol program. Sndvol modifies only the master volume levels of sessions. By default, the session manager sets the per-channel volume levels to 1.0 at the initial activation of a session. Subsequent per-channel volume changes by clients are persistent across computer restarts.

When releasing an <b>IChannelAudioVolume</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

The <b>IChannelAudioVolume</b> interface controls the channel volumes in an audio session. An audio session is a collection of shared-mode streams. This interface does not work with exclusive-mode streams. For information about volume controls for exclusive-mode streams, see <a href="/windows/desktop/CoreAudio/endpointvolume-api">EndpointVolume API</a>.

## -inheritance

The <b>IChannelAudioVolume</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IChannelAudioVolume</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiostreamvolume">IAudioStreamVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-isimpleaudiovolume">ISimpleAudioVolume Interface</a>



<a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a>
