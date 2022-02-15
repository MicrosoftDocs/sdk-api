---
UID: NF:audiopolicy.IAudioVolumeDuckNotification.OnVolumeUnduckNotification
title: IAudioVolumeDuckNotification::OnVolumeUnduckNotification (audiopolicy.h)
description: The OnVolumeUnduckNotification method sends a notification about a pending system unducking event.
helpviewer_keywords: ["IAudioVolumeDuckNotification interface [Core Audio]","OnVolumeUnduckNotification method","IAudioVolumeDuckNotification.OnVolumeUnduckNotification","IAudioVolumeDuckNotification::OnVolumeUnduckNotification","OnVolumeUnduckNotification","OnVolumeUnduckNotification method [Core Audio]","OnVolumeUnduckNotification method [Core Audio]","IAudioVolumeDuckNotification interface","audiopolicy/IAudioVolumeDuckNotification::OnVolumeUnduckNotification","coreaudio.iaudiovolumeducknotification_onvolumeunducknotification"]
old-location: coreaudio\iaudiovolumeducknotification_onvolumeunducknotification.htm
tech.root: CoreAudio
ms.assetid: f25f066e-999f-45ff-8287-afa8acb82a19
ms.date: 12/05/2018
ms.keywords: IAudioVolumeDuckNotification interface [Core Audio],OnVolumeUnduckNotification method, IAudioVolumeDuckNotification.OnVolumeUnduckNotification, IAudioVolumeDuckNotification::OnVolumeUnduckNotification, OnVolumeUnduckNotification, OnVolumeUnduckNotification method [Core Audio], OnVolumeUnduckNotification method [Core Audio],IAudioVolumeDuckNotification interface, audiopolicy/IAudioVolumeDuckNotification::OnVolumeUnduckNotification, coreaudio.iaudiovolumeducknotification_onvolumeunducknotification
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
 - IAudioVolumeDuckNotification::OnVolumeUnduckNotification
 - audiopolicy/IAudioVolumeDuckNotification::OnVolumeUnduckNotification
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
 - IAudioVolumeDuckNotification.OnVolumeUnduckNotification
---

## -description

The <b>OnVolumeUnduckNotification</b> method sends a notification about a pending system unducking event. For more information, see <a href="/windows/desktop/CoreAudio/handling-audio-ducking-events-from-communication-devices">Implementation Considerations for Ducking Notifications</a>.

## -parameters

### -param sessionID [in]

A string containing the session instance identifier of the terminating communications session that initiated the ducking. To get the session instance identifier, call <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier">IAudioSessionControl2::GetSessionInstanceIdentifier</a>.

## -returns

If the method succeeds, it returns S_OK.

## -remarks

After the application registers its implementation  of the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiovolumeducknotification">IAudioVolumeDuckNotification</a> interface by calling <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification">IAudioSessionManager2::RegisterDuckNotification</a>, the session manager calls <b>OnVolumeUnduckNotification</b> when it wants to send a notification about when ducking ends. The application receives the event notifications in the form of callbacks.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiovolumeducknotification">IAudioVolumeDuckNotification</a>

<a href="/windows/desktop/CoreAudio/using-the-communication-device">Using a Communication Device</a>