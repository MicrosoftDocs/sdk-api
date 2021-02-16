---
UID: NF:audiopolicy.IAudioSessionManager2.UnregisterSessionNotification
title: IAudioSessionManager2::UnregisterSessionNotification (audiopolicy.h)
description: The UnregisterSessionNotification method deletes the registration to receive a notification when a session is created.
helpviewer_keywords: ["IAudioSessionManager2 interface [Core Audio]","UnregisterSessionNotification method","IAudioSessionManager2.UnregisterSessionNotification","IAudioSessionManager2::UnregisterSessionNotification","UnregisterSessionNotification","UnregisterSessionNotification method [Core Audio]","UnregisterSessionNotification method [Core Audio]","IAudioSessionManager2 interface","audiopolicy/IAudioSessionManager2::UnregisterSessionNotification","coreaudio.iaudiosessionmanager2_unregistersessionnotification"]
old-location: coreaudio\iaudiosessionmanager2_unregistersessionnotification.htm
tech.root: CoreAudio
ms.assetid: 0c334963-2b60-4eb1-b8a2-c9ed0d21bd5e
ms.date: 12/05/2018
ms.keywords: IAudioSessionManager2 interface [Core Audio],UnregisterSessionNotification method, IAudioSessionManager2.UnregisterSessionNotification, IAudioSessionManager2::UnregisterSessionNotification, UnregisterSessionNotification, UnregisterSessionNotification method [Core Audio], UnregisterSessionNotification method [Core Audio],IAudioSessionManager2 interface, audiopolicy/IAudioSessionManager2::UnregisterSessionNotification, coreaudio.iaudiosessionmanager2_unregistersessionnotification
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
 - IAudioSessionManager2::UnregisterSessionNotification
 - audiopolicy/IAudioSessionManager2::UnregisterSessionNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiopolicy.h
api_name:
 - IAudioSessionManager2.UnregisterSessionNotification
---

# IAudioSessionManager2::UnregisterSessionNotification


## -description

The <b>UnregisterSessionNotification</b> method deletes the registration to  receive a notification when a session is created.

## -parameters

### -param SessionNotification

A pointer to the application's implementation of the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a> interface. Pass the same interface pointer that was specified to the session manager in  a previous call to <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registersessionnotification">IAudioSessionManager2::RegisterSessionNotification</a> to register for notification.  

If the <b>UnregisterSessionNotification</b> method succeeds, it calls the <b>Release</b> method on the application's <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a> interface.

## -returns

If the method succeeds, it returns S_OK.
          If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_POINTER</dt>
</dl>
</td>
<td width="60%">
<i>SessionNotification</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The application calls this method when it no longer needs to receive notifications. The <b>UnregisterSessionNotification</b> method removes the registration of an <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a> interface that the application previously registered with the session manager by calling the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification">IAudioSessionControl::RegisterAudioSessionNotification</a> method.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2">IAudioSessionManager2</a>