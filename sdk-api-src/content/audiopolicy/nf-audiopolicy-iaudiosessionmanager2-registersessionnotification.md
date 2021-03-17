---
UID: NF:audiopolicy.IAudioSessionManager2.RegisterSessionNotification
title: IAudioSessionManager2::RegisterSessionNotification (audiopolicy.h)
description: The RegisterSessionNotification method registers the application to receive a notification when a session is created.
helpviewer_keywords: ["IAudioSessionManager2 interface [Core Audio]","RegisterSessionNotification method","IAudioSessionManager2.RegisterSessionNotification","IAudioSessionManager2::RegisterSessionNotification","RegisterSessionNotification","RegisterSessionNotification method [Core Audio]","RegisterSessionNotification method [Core Audio]","IAudioSessionManager2 interface","audiopolicy/IAudioSessionManager2::RegisterSessionNotification","coreaudio.iaudiosessionmanager2_registersessionnotification"]
old-location: coreaudio\iaudiosessionmanager2_registersessionnotification.htm
tech.root: CoreAudio
ms.assetid: cff43da7-70b2-4887-8a6c-6100cf7d696e
ms.date: 12/05/2018
ms.keywords: IAudioSessionManager2 interface [Core Audio],RegisterSessionNotification method, IAudioSessionManager2.RegisterSessionNotification, IAudioSessionManager2::RegisterSessionNotification, RegisterSessionNotification, RegisterSessionNotification method [Core Audio], RegisterSessionNotification method [Core Audio],IAudioSessionManager2 interface, audiopolicy/IAudioSessionManager2::RegisterSessionNotification, coreaudio.iaudiosessionmanager2_registersessionnotification
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
 - IAudioSessionManager2::RegisterSessionNotification
 - audiopolicy/IAudioSessionManager2::RegisterSessionNotification
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
 - IAudioSessionManager2.RegisterSessionNotification
---

# IAudioSessionManager2::RegisterSessionNotification


## -description

The <b>RegisterSessionNotification</b> method registers the application to receive a notification when a session is created.

## -parameters

### -param SessionNotification

A pointer to the application's implementation of the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a> interface. If the method call succeeds, it calls the <b>AddRef</b> method on the application's <b>IAudioSessionNotification</b> interface.

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
<tr>
<td width="40%">
<dl>
<dt>E_OUTOFMEMORY</dt>
</dl>
</td>
<td width="60%">
Internal object could not be created due to insufficient memory.

</td>
</tr>
</table>

## -remarks

The application can register to receive a notification  when a session is created, through the methods  of the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a> interface.  The application implements the <b>IAudioSessionNotification</b> interface. The methods defined in this interface receive callbacks from the  system when a session is created. For example code that shows how to implement this interface, see 

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification Interface</a>.

To begin receiving notifications, the application calls the <b>IAudioSessionManager2::RegisterSessionNotification</b> method to register its <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification">IAudioSessionNotification</a> interface. When the application no longer requires notifications, it calls the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregistersessionnotification">IAudioSessionManager2::UnregisterSessionNotification</a> method to delete the registration.

> [!Important]
> You must call [IAudioSessionEnumerator::GetCount](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionenumerator-getcount) to begin receiving notifications. The session enumeration API discards new session notifications until the application has first retrieved the list of existing sessions. This is to prevent a race condition that can occur when a session notification arrives while the application using the session APIs is starting up. Calling **GetCount** triggers the enumeration API to begin sending session notifications.

<div class="alert"><b>Note</b>  Make sure that the application initializes COM with Multithreaded Apartment (MTA) model by calling <code>CoInitializeEx(NULL, COINIT_MULTITHREADED)</code> in a non-UI thread. If MTA is not initialized, the application does not receive session notifications from the session manager. 
Threads that run the user interface of an application should be initialized apartment threading model.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2">IAudioSessionManager2</a>