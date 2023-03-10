---
UID: NF:audiopolicy.IAudioSessionEvents.OnDisplayNameChanged
title: IAudioSessionEvents::OnDisplayNameChanged (audiopolicy.h)
description: The OnDisplayNameChanged method notifies the client that the display name for the session has changed.
helpviewer_keywords: ["IAudioSessionEvents interface [Core Audio]","OnDisplayNameChanged method","IAudioSessionEvents.OnDisplayNameChanged","IAudioSessionEvents::OnDisplayNameChanged","IAudioSessionEventsOnDisplayNameChanged","OnDisplayNameChanged","OnDisplayNameChanged method [Core Audio]","OnDisplayNameChanged method [Core Audio]","IAudioSessionEvents interface","audiopolicy/IAudioSessionEvents::OnDisplayNameChanged","coreaudio.iaudiosessionevents_ondisplaynamechanged"]
old-location: coreaudio\iaudiosessionevents_ondisplaynamechanged.htm
tech.root: CoreAudio
ms.assetid: 65d21f0c-b6f1-4506-975c-6d0308b3fc2f
ms.date: 12/05/2018
ms.keywords: IAudioSessionEvents interface [Core Audio],OnDisplayNameChanged method, IAudioSessionEvents.OnDisplayNameChanged, IAudioSessionEvents::OnDisplayNameChanged, IAudioSessionEventsOnDisplayNameChanged, OnDisplayNameChanged, OnDisplayNameChanged method [Core Audio], OnDisplayNameChanged method [Core Audio],IAudioSessionEvents interface, audiopolicy/IAudioSessionEvents::OnDisplayNameChanged, coreaudio.iaudiosessionevents_ondisplaynamechanged
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
 - IAudioSessionEvents::OnDisplayNameChanged
 - audiopolicy/IAudioSessionEvents::OnDisplayNameChanged
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
 - IAudioSessionEvents.OnDisplayNameChanged
---

# IAudioSessionEvents::OnDisplayNameChanged


## -description

The <b>OnDisplayNameChanged</b> method notifies the client that the display name for the session has changed.

## -parameters

### -param NewDisplayName [in]

The new display name for the session. This parameter points to a null-terminated, wide-character string containing the new display name. The string remains valid for the duration of the call.

### -param EventContext [in]

The event context value. This is the same value that the caller passed to <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setdisplayname">IAudioSessionControl::SetDisplayName</a> in the call that changed the display name for the session. For more information, see Remarks.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The session manager calls this method each time a call to the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setdisplayname">IAudioSessionControl::SetDisplayName</a> method changes the display name of the session. The Sndvol program uses a session's display name to label the volume slider for the session.

The <i>EventContext</i> parameter provides a means for a client to distinguish between a display-name change that it initiated and one that some other client initiated. When calling the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setdisplayname">IAudioSessionControl::SetDisplayName</a> method, a client passes in an <i>EventContext</i> parameter value that its implementation of the <b>OnDisplayNameChanged</b> method can recognize.

For a code example that implements the methods in the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents</a> interface, see <a href="/windows/desktop/CoreAudio/audio-session-events">Audio Session Events</a>.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setdisplayname">IAudioSessionControl::SetDisplayName</a>



<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionevents">IAudioSessionEvents Interface</a>