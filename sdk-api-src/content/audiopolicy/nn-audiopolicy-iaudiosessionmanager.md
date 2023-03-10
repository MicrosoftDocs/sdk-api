---
UID: NN:audiopolicy.IAudioSessionManager
title: IAudioSessionManager (audiopolicy.h)
description: The IAudioSessionManager interface enables a client to access the session controls and volume controls for both cross-process and process-specific audio sessions.
helpviewer_keywords: ["IAudioSessionManager","IAudioSessionManager interface [Core Audio]","IAudioSessionManager interface [Core Audio]","described","audiopolicy/IAudioSessionManager","coreaudio.iaudiosessionmanager"]
old-location: coreaudio\iaudiosessionmanager.htm
tech.root: CoreAudio
ms.assetid: 606b0a42-d1d1-4196-911f-5b095bf56c4e
ms.date: 12/05/2018
ms.keywords: IAudioSessionManager, IAudioSessionManager interface [Core Audio], IAudioSessionManager interface [Core Audio],described, audiopolicy/IAudioSessionManager, coreaudio.iaudiosessionmanager
req.header: audiopolicy.h
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
 - IAudioSessionManager
 - audiopolicy/IAudioSessionManager
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
 - IAudioSessionManager
---

# IAudioSessionManager interface


## -description

The <b>IAudioSessionManager</b> interface enables a client to access the session controls and volume controls for both cross-process and process-specific audio sessions. The client obtains a reference to an <b>IAudioSessionManager</b> interface by calling the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a> method with parameter <i>iid</i> set to <b>REFIID</b> IID_IAudioSessionManager.

This interface enables clients to access the controls for an existing session without first opening a stream. This capability is useful for clients of higher-level APIs that are built on top of WASAPI and use session controls internally but do not give their clients access to session controls.

In Windows Vista, the higher-level APIs that use WASAPI include Media Foundation, DirectSound, the Windows multimedia <b>waveInXxx</b>, <b>waveOutXxx</b>, and <b>mciXxx</b> functions, and third-party APIs.

When a client creates an audio stream through a higher-level API, that API typically adds the stream to the default audio session for the client's process (the session that is identified by the session GUID value, GUID_NULL), but the same API might not provide a means for the client to access the controls for that session. In that case, the client can access the controls through the <b>IAudioSessionManager</b> interface.

For a code example that uses the <b>IAudioSessionManager</b> interface, see <a href="/windows/desktop/CoreAudio/audio-events-for-legacy-audio-applications">Audio Events for Legacy Audio Applications</a>.

## -inheritance

The <b>IAudioSessionManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioSessionManager</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>



<a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a>
