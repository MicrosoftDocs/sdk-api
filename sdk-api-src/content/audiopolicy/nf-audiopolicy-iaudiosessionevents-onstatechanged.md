---
UID: NF:audiopolicy.IAudioSessionEvents.OnStateChanged
title: IAudioSessionEvents::OnStateChanged (audiopolicy.h)
description: The OnStateChanged method notifies the client that the stream-activity state of the session has changed.
helpviewer_keywords: ["IAudioSessionEvents interface [Core Audio]","OnStateChanged method","IAudioSessionEvents.OnStateChanged","IAudioSessionEvents::OnStateChanged","IAudioSessionEventsOnStateChanged","OnStateChanged","OnStateChanged method [Core Audio]","OnStateChanged method [Core Audio]","IAudioSessionEvents interface","audiopolicy/IAudioSessionEvents::OnStateChanged","coreaudio.iaudiosessionevents_onstatechanged"]
old-location: coreaudio\iaudiosessionevents_onstatechanged.htm
tech.root: CoreAudio
ms.assetid: 4ec3e676-cf08-4041-b5bf-5cb429569e03
ms.date: 12/05/2018
ms.keywords: IAudioSessionEvents interface [Core Audio],OnStateChanged method, IAudioSessionEvents.OnStateChanged, IAudioSessionEvents::OnStateChanged, IAudioSessionEventsOnStateChanged, OnStateChanged, OnStateChanged method [Core Audio], OnStateChanged method [Core Audio],IAudioSessionEvents interface, audiopolicy/IAudioSessionEvents::OnStateChanged, coreaudio.iaudiosessionevents_onstatechanged
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
 - IAudioSessionEvents::OnStateChanged
 - audiopolicy/IAudioSessionEvents::OnStateChanged
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
 - IAudioSessionEvents.OnStateChanged
---

# IAudioSessionEvents::OnStateChanged


## -description

The <b>OnStateChanged</b> method notifies the client that the stream-activity state of the session has changed.

## -parameters

### -param NewState [in]

The new session state. The value of this parameter is one of the following <a href="/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audiosessionstate">AudioSessionState</a> enumeration values:

AudioSessionStateActive

AudioSessionStateInactive

AudioSessionStateExpired

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

A client cannot generate a session-state-change event. The system is always the source of this type of event. Thus, unlike some other <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> methods, this method does not supply a context parameter.

The system changes the state of a session from inactive to active at the time that a client opens the first stream in the session. A client opens a stream by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method. The system changes the session state from active to inactive at the time that a client closes the last stream in the session. The client that releases the last reference to an <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> object closes the stream that is associated with the object.

For a code example that implements the methods in the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interface, see <a href="/windows/desktop/CoreAudio/audio-session-events">Audio Session Events</a>.

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>