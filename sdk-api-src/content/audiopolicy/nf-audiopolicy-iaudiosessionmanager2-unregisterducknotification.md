---
UID: NF:audiopolicy.IAudioSessionManager2.UnregisterDuckNotification
title: IAudioSessionManager2::UnregisterDuckNotification (audiopolicy.h)
description: The UnregisterDuckNotification method deletes a previous registration by the application to receive notifications.
helpviewer_keywords: ["IAudioSessionManager2 interface [Core Audio]","UnregisterDuckNotification method","IAudioSessionManager2.UnregisterDuckNotification","IAudioSessionManager2::UnregisterDuckNotification","UnregisterDuckNotification","UnregisterDuckNotification method [Core Audio]","UnregisterDuckNotification method [Core Audio]","IAudioSessionManager2 interface","audiopolicy/IAudioSessionManager2::UnregisterDuckNotification","coreaudio.iaudiosessionmanager2_unregisterducknotification"]
old-location: coreaudio\iaudiosessionmanager2_unregisterducknotification.htm
tech.root: CoreAudio
ms.assetid: 0ab0f5d0-8831-41a2-bfee-3e88a3d92156
ms.date: 12/05/2018
ms.keywords: IAudioSessionManager2 interface [Core Audio],UnregisterDuckNotification method, IAudioSessionManager2.UnregisterDuckNotification, IAudioSessionManager2::UnregisterDuckNotification, UnregisterDuckNotification, UnregisterDuckNotification method [Core Audio], UnregisterDuckNotification method [Core Audio],IAudioSessionManager2 interface, audiopolicy/IAudioSessionManager2::UnregisterDuckNotification, coreaudio.iaudiosessionmanager2_unregisterducknotification
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
 - IAudioSessionManager2::UnregisterDuckNotification
 - audiopolicy/IAudioSessionManager2::UnregisterDuckNotification
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
 - IAudioSessionManager2.UnregisterDuckNotification
---

# IAudioSessionManager2::UnregisterDuckNotification


## -description

The <b>UnregisterDuckNotification</b> method deletes a previous registration by the application to receive notifications.

## -parameters

### -param duckNotification

Pointer to the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiovolumeducknotification">IAudioVolumeDuckNotification</a> interface that is implemented by the application. Pass the same interface pointer that was specified to the session manager in a previous call to the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification">IAudioSessionManager2::RegisterDuckNotification</a> method. If the <b>UnregisterDuckNotification</b> method succeeds, it calls the <b>Release</b> method on the application's <b>IAudioVolumeDuckNotification</b> interface.

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
<i>duckNotification</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The application calls this method when it no longer needs to receive notifications. The <b>UnregisterDuckNotification</b> method removes the registration of an <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiovolumeducknotification">IAudioVolumeDuckNotification</a> interface that the application previously registered with the session manager by calling the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification">IAudioSessionManager2::RegisterDuckNotification</a> method.

After the application calls <b>UnregisterDuckNotification</b>, any pending events are not reported to the application.

## -see-also

<a href="/windows/desktop/CoreAudio/stream-attenuation">Default Ducking Experience</a>



<a href="/windows/desktop/CoreAudio/handling-audio-ducking-events-from-communication-devices">Getting Ducking Events</a>



<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2">IAudioSessionManager2</a>