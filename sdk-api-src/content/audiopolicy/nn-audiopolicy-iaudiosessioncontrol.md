---
UID: NN:audiopolicy.IAudioSessionControl
title: IAudioSessionControl (audiopolicy.h)
description: The IAudioSessionControl interface enables a client to configure the control parameters for an audio session and to monitor events in the session.
helpviewer_keywords: ["IAudioSessionControl","IAudioSessionControl interface [Core Audio]","IAudioSessionControl interface [Core Audio]","described","audiopolicy/IAudioSessionControl","coreaudio.iaudiosessioncontrol"]
old-location: coreaudio\iaudiosessioncontrol.htm
tech.root: CoreAudio
ms.assetid: 4446140e-2e61-40ed-b0f9-4c1b90e7c2de
ms.date: 12/05/2018
ms.keywords: IAudioSessionControl, IAudioSessionControl interface [Core Audio], IAudioSessionControl interface [Core Audio],described, audiopolicy/IAudioSessionControl, coreaudio.iaudiosessioncontrol
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
 - IAudioSessionControl
 - audiopolicy/IAudioSessionControl
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
 - IAudioSessionControl
---

# IAudioSessionControl interface


## -description

The <b>IAudioSessionControl</b> interface enables a client to configure the control parameters for an <a href="/windows/desktop/CoreAudio/audio-sessions">audio session</a> and to monitor events in the session. The <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method initializes a stream object and assigns the stream to an audio session. The client obtains a reference to the <b>IAudioSessionControl</b> interface on a stream object by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a> method with parameter <i>riid</i> set to <b>REFIID</b> IID_IAudioSessionControl.

Alternatively, a client can obtain the <b>IAudioSessionControl</b> interface of an existing session without having to first create a stream object and add the stream to the session. Instead, the client calls the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol">IAudioSessionManager::GetAudioSessionControl</a> method with parameter <i>AudioSessionGuid</i> set to the session GUID.

The client can register to receive notification from the session manager when clients change session parameters through the methods in the <b>IAudioSessionControl</b> interface.

When releasing an <b>IAudioSessionControl</b> interface instance, the client must call the interface's <b>Release</b> method from the same thread as the call to <b>IAudioClient::GetService</b> that created the object.

The <b>IAudioSessionControl</b> interface controls an audio session. An audio session is a collection of shared-mode streams. This interface does not work with exclusive-mode streams.

For a code example that uses the <b>IAudioSessionControl</b> interface, see <a href="/windows/desktop/CoreAudio/audio-events-for-legacy-audio-applications">Audio Events for Legacy Audio Applications</a>.

## -inheritance

The <b>IAudioSessionControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioSessionControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getservice">IAudioClient::GetService</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol">IAudioSessionManager::GetAudioSessionControl</a>



<a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a>
