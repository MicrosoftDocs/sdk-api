---
UID: NE:audiosessiontypes._AudioSessionState
title: AudioSessionState (audiosessiontypes.h)
description: The AudioSessionState enumeration defines constants that indicate the current state of an audio session.
helpviewer_keywords: ["AudioSessionState","AudioSessionState","AudioSessionState enumeration [Core Audio]","AudioSessionStateActive","AudioSessionStateExpired","AudioSessionStateInactive","audiosessiontypes/AudioSessionState","audiosessiontypes/AudioSessionStateActive","audiosessiontypes/AudioSessionStateExpired","audiosessiontypes/AudioSessionStateInactive","coreaudio.audiosessionstate"]
old-location: coreaudio\audiosessionstate.htm
tech.root: CoreAudio
ms.assetid: a972fed6-425f-46c8-b0cc-6538460bb104
ms.date: 12/05/2018
ms.keywords: AudioSessionState, AudioSessionState , AudioSessionState enumeration [Core Audio], AudioSessionStateActive, AudioSessionStateExpired, AudioSessionStateInactive, audiosessiontypes/AudioSessionState, audiosessiontypes/AudioSessionStateActive, audiosessiontypes/AudioSessionStateExpired, audiosessiontypes/AudioSessionStateInactive, coreaudio.audiosessionstate
req.header: audiosessiontypes.h
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
req.typenames: AudioSessionState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AudioSessionState
 - audiosessiontypes/_AudioSessionState
 - AudioSessionState
 - audiosessiontypes/AudioSessionState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audiosessiontypes.h
api_name:
 - AudioSessionState
---

# AudioSessionState enumeration


## -description

The <b>AudioSessionState</b> enumeration defines constants that indicate the current state of an audio session.

## -enum-fields

### -field AudioSessionStateInactive

The audio session is inactive. (It contains at least one stream, but none of the streams in the session is currently running.)

### -field AudioSessionStateActive

The audio session is active. (At least one of the streams in the session is running.)

### -field AudioSessionStateExpired

The audio session has expired. (It contains no streams.)

## -remarks

When a client opens a session by assigning the first stream to the session (by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method), the initial session state is inactive. The session state changes from inactive to active when a stream in the session begins running (because the client has called the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">IAudioClient::Start</a> method). The session changes from active to inactive when the client stops the last running stream in the session (by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-stop">IAudioClient::Stop</a> method). The session state changes to expired when the client destroys the last stream in the session by releasing all references to the stream object.

The system volume-control program, Sndvol, displays volume controls for both active and inactive sessions. Sndvol stops displaying the volume control for a session when the session state changes to expired. For more information about Sndvol, see <a href="/windows/desktop/CoreAudio/audio-sessions">Audio Sessions</a>.

The <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getstate">IAudioSessionControl::GetState</a> and <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged">IAudioSessionEvents::OnStateChanged</a> methods use the constants defined in the <b>AudioSessionState</b> enumeration.

For more information about session states, see <a href="/windows/desktop/CoreAudio/audio-sessions">Audio Sessions</a>.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-constants">Core Audio Constants</a>



<a href="/windows/desktop/CoreAudio/core-audio-enumerations">Core Audio Enumerations</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">IAudioClient::Start</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-stop">IAudioClient::Stop</a>



<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getstate">IAudioSessionControl::GetState</a>



<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged">IAudioSessionEvents::OnStateChanged</a>