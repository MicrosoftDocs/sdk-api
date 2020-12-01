---
UID: NF:audiopolicy.IAudioVolumeDuckNotification.OnVolumeDuckNotification
title: IAudioVolumeDuckNotification::OnVolumeDuckNotification (audiopolicy.h)
description: The OnVolumeDuckNotification method sends a notification about a pending system ducking event.
helpviewer_keywords: ["IAudioVolumeDuckNotification interface [Core Audio]","OnVolumeDuckNotification method","IAudioVolumeDuckNotification.OnVolumeDuckNotification","IAudioVolumeDuckNotification::OnVolumeDuckNotification","OnVolumeDuckNotification","OnVolumeDuckNotification method [Core Audio]","OnVolumeDuckNotification method [Core Audio]","IAudioVolumeDuckNotification interface","audiopolicy/IAudioVolumeDuckNotification::OnVolumeDuckNotification","coreaudio.iaudiovolumeducknotification_onvolumeducknotification"]
old-location: coreaudio\iaudiovolumeducknotification_onvolumeducknotification.htm
tech.root: CoreAudio
ms.assetid: 1bc28f44-1595-4d45-872f-2473bffd33aa
ms.date: 12/05/2018
ms.keywords: IAudioVolumeDuckNotification interface [Core Audio],OnVolumeDuckNotification method, IAudioVolumeDuckNotification.OnVolumeDuckNotification, IAudioVolumeDuckNotification::OnVolumeDuckNotification, OnVolumeDuckNotification, OnVolumeDuckNotification method [Core Audio], OnVolumeDuckNotification method [Core Audio],IAudioVolumeDuckNotification interface, audiopolicy/IAudioVolumeDuckNotification::OnVolumeDuckNotification, coreaudio.iaudiovolumeducknotification_onvolumeducknotification
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IAudioVolumeDuckNotification::OnVolumeDuckNotification
 - audiopolicy/IAudioVolumeDuckNotification::OnVolumeDuckNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AudioPolicy.h
api_name:
 - IAudioVolumeDuckNotification.OnVolumeDuckNotification
---

## -description

The <b>OnVolumeDuckNotification</b> method sends a notification about a pending system ducking event. For more information, see <a href="/windows/desktop/CoreAudio/handling-audio-ducking-events-from-communication-devices">Implementation considerations for ducking notifications</a>.

## -parameters

### -param sessionID [in]

A string containing the session instance identifier of the communications session that raises the  the auto-ducking event. To get the session instance identifier, call <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier">IAudioSessionControl2::GetSessionInstanceIdentifier</a>.

### -param countCommunicationSessions [in]

The number of active communications sessions. If there are n sessions, the sessions are numbered from 0 to –1.

## -returns

If the method succeeds, it returns S_OK.

## -remarks

After the application registers its implementation  of the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiovolumeducknotification">IAudioVolumeDuckNotification</a> interface by calling <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification">IAudioSessionManager2::RegisterDuckNotification</a>, the session manager calls <b>OnVolumeDuckNotification</b> when it wants to send a notification about when ducking begins. The application receives the event notifications in the form of callbacks.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiovolumeducknotification">IAudioVolumeDuckNotification</a>

<a href="/windows/desktop/CoreAudio/using-the-communication-device">Using a Communication Device</a>