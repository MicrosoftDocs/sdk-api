---
UID: NN:audioclient.ISimpleAudioVolume
title: ISimpleAudioVolume (audioclient.h)
description: The ISimpleAudioVolume interface enables a client to control the master volume level of an audio session.
helpviewer_keywords: ["ISimpleAudioVolume","ISimpleAudioVolume interface [Core Audio]","ISimpleAudioVolume interface [Core Audio]","described","audioclient/ISimpleAudioVolume","coreaudio.isimpleaudiovolume"]
old-location: coreaudio\isimpleaudiovolume.htm
tech.root: CoreAudio
ms.assetid: 360211f2-de82-4ff5-896c-dee1d60cb7b7
ms.date: 12/05/2018
ms.keywords: ISimpleAudioVolume, ISimpleAudioVolume interface [Core Audio], ISimpleAudioVolume interface [Core Audio],described, audioclient/ISimpleAudioVolume, coreaudio.isimpleaudiovolume
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
 - ISimpleAudioVolume
 - audioclient/ISimpleAudioVolume
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
 - ISimpleAudioVolume
---

# ISimpleAudioVolume interface


## -description

The <b>ISimpleAudioVolume</b> interface enables a client to control the master volume level of an <a href="/windows/desktop/CoreAudio/audio-sessions">audio session</a>. The <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method initializes a stream object and assigns the stream to an audio session. The client obtains a reference to the <b>ISimpleAudioVolume</b> interface on a stream object by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to <b>REFIID</b> IID_ISimpleAudioVolume.

Alternatively, a client can obtain the <b>ISimpleAudioVolume</b> interface of an existing session without having to first create a stream object and add the stream to the session. Instead, the client calls the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager-getsimpleaudiovolume">IAudioSessionManager::GetSimpleAudioVolume</a> method with the session GUID.

The effective volume level of any channel in the session submix, as heard at the speakers, is the product of the following four volume-level factors:

<ul>
<li>The per-channel volume levels of the streams in the session, which clients can control through the methods in the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiostreamvolume">IAudioStreamVolume</a> interface.</li>
<li>The master volume level of the session, which clients can control through the methods in the <b>ISimpleAudioVolume</b> interface.</li>
<li>The per-channel volume level of the session, which clients can control through the methods in the <a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume</a> interface.</li>
<li>The policy-based volume level of the session, which the system dynamically assigns to the session as the global mix changes.</li>
</ul>
Each of the four volume-level factors in the preceding list is a value in the range 0.0 to 1.0, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation). The effective volume level is also a value in the range 0.0 to 1.0.

Typical audio applications do not modify the volume levels of sessions. Instead, they rely on users to set these volume levels through the Sndvol program. Sndvol modifies only the master volume levels of sessions. By default, the session manager sets the master volume level to 1.0 at the initial activation of a session. Subsequent volume changes by Sndvol or other clients are persistent across computer restarts.

When releasing an <b>ISimpleAudioVolume</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

The <b>ISimpleAudioVolume</b> interface controls the volume of an audio session. An audio session is a collection of shared-mode streams. This interface does not work with exclusive-mode streams. For information about volume controls for exclusive-mode streams, see <a href="/windows/desktop/CoreAudio/endpointvolume-api">EndpointVolume API</a>.

## -inheritance

The <b>ISimpleAudioVolume</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISimpleAudioVolume</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiostreamvolume">IAudioStreamVolume Interface</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-ichannelaudiovolume">IChannelAudioVolume Interface</a>



<a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a>
