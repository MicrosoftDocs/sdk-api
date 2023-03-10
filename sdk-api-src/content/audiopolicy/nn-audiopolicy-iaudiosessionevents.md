---
UID: NN:audiopolicy.IAudioSessionEvents
title: IAudioSessionEvents (audiopolicy.h)
description: The IAudioSessionEvents interface provides notifications of session-related events such as changes in the volume level, display name, and session state.
helpviewer_keywords: ["IAudioSessionEvents","IAudioSessionEvents interface [Core Audio]","IAudioSessionEvents interface [Core Audio]","described","audiopolicy/IAudioSessionEvents","coreaudio.iaudiosessionevents"]
old-location: coreaudio\iaudiosessionevents.htm
tech.root: CoreAudio
ms.assetid: fd287ef7-8a37-4342-b4c2-79b84a56c30e
ms.date: 12/05/2018
ms.keywords: IAudioSessionEvents, IAudioSessionEvents interface [Core Audio], IAudioSessionEvents interface [Core Audio],described, audiopolicy/IAudioSessionEvents, coreaudio.iaudiosessionevents
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
 - IAudioSessionEvents
 - audiopolicy/IAudioSessionEvents
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
 - IAudioSessionEvents
---

# IAudioSessionEvents interface


## -description

The <b>IAudioSessionEvents</b> interface provides notifications of session-related events such as changes in the volume level, display name, and session state. Unlike the other interfaces in this section, which are implemented by the WASAPI system component, a WASAPI client implements the <b>IAudioSessionEvents</b> interface. To receive event notifications, the client passes a pointer to its <b>IAudioSessionEvents</b> interface to the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification">IAudioSessionControl::RegisterAudioSessionNotification</a> method.

After registering its <b>IAudioClientSessionEvents</b> interface, the client receives event notifications in the form of callbacks through the methods in the interface.

In implementing the <b>IAudioSessionEvents</b> interface, the client should observe these rules to avoid deadlocks and undefined behavior:

<ul>
<li>The methods in the interface must be nonblocking. The client should never wait on a synchronization object during an event callback.</li>
<li>The client should never call the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification">IAudioSessionControl::UnregisterAudioSessionNotification</a> method during an event callback.</li>
<li>The client should never release the final reference on a WASAPI object during an event callback.</li>
</ul>
For a code example that implements an <b>IAudioSessionEvents</b> interface, see <a href="/windows/desktop/CoreAudio/audio-session-events">Audio Session Events</a>. For a code example that registers a client's <b>IAudioSessionEvents</b> interface to receive notifications, see <a href="/windows/desktop/CoreAudio/audio-events-for-legacy-audio-applications">Audio Events for Legacy Audio Applications</a>.

## -inheritance

The <b>IAudioSessionEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAudioSessionEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification">IAudioSessionControl::RegisterAudioSessionNotification</a>



<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification">IAudioSessionControl::UnregisterAudioSessionNotification</a>



<a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a>
