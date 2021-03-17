---
UID: NF:audiopolicy.IAudioSessionManager2.RegisterDuckNotification
title: IAudioSessionManager2::RegisterDuckNotification (audiopolicy.h)
description: The RegisterDuckNotification method registers the application with the session manager to receive ducking notifications.
helpviewer_keywords: ["IAudioSessionManager2 interface [Core Audio]","RegisterDuckNotification method","IAudioSessionManager2.RegisterDuckNotification","IAudioSessionManager2::RegisterDuckNotification","RegisterDuckNotification","RegisterDuckNotification method [Core Audio]","RegisterDuckNotification method [Core Audio]","IAudioSessionManager2 interface","audiopolicy/IAudioSessionManager2::RegisterDuckNotification","coreaudio.iaudiosessionmanager2_registerducknotification"]
old-location: coreaudio\iaudiosessionmanager2_registerducknotification.htm
tech.root: CoreAudio
ms.assetid: bed27f3f-6293-4a25-baa0-39562d45bddc
ms.date: 12/05/2018
ms.keywords: IAudioSessionManager2 interface [Core Audio],RegisterDuckNotification method, IAudioSessionManager2.RegisterDuckNotification, IAudioSessionManager2::RegisterDuckNotification, RegisterDuckNotification, RegisterDuckNotification method [Core Audio], RegisterDuckNotification method [Core Audio],IAudioSessionManager2 interface, audiopolicy/IAudioSessionManager2::RegisterDuckNotification, coreaudio.iaudiosessionmanager2_registerducknotification
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
 - IAudioSessionManager2::RegisterDuckNotification
 - audiopolicy/IAudioSessionManager2::RegisterDuckNotification
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
 - IAudioSessionManager2.RegisterDuckNotification
---

# IAudioSessionManager2::RegisterDuckNotification


## -description

The <b>RegisterDuckNotification</b> method registers the application with the session manager to receive ducking notifications.

## -parameters

### -param sessionID

Pointer to a null-terminated string that contains a  session instance identifier. Applications that are playing a media stream and want to provide custom stream attenuation or ducking behavior, pass their own session instance identifier.  For more information, see Remarks.

Other applications
    that do not want to alter their streams but want to get all the ducking notifications
    must pass <b>NULL</b>.

### -param duckNotification

Pointer to the application's implementation of the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiovolumeducknotification">IAudioVolumeDuckNotification</a> interface. The implementation is called when ducking events are raised by the audio system and  notifications are sent to the registered applications.

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

<i>Stream Attenuation</i> or <i>ducking</i> is a new feature in Windows 7. An application playing a media stream can make the stream behave differently when a new communication stream is opened on the default communication device. For example, the original media stream can be paused while the new communication stream is open. To provide this custom implementation for stream attenuation, the application can opt out of the default stream attenuation experience by calling <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference">IAudioSessionControl::SetDuckingPreference</a> and then register itself to receive notifications when session events occur. For stream attenuation, a session event is raised by the system when a communication stream is opened or closed on the default communication device. For more information about this feature, see <a href="/windows/desktop/CoreAudio/handling-audio-ducking-events-from-communication-devices">Getting Ducking Events</a>.

To begin receiving notifications, the application calls the <b>RegisterDuckNotification</b> method to register its <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiovolumeducknotification">IAudioVolumeDuckNotification</a> interface with the session manager. When the application no longer requires notifications, it calls the <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification">IAudioSessionManager2::UnregisterDuckNotification</a> method to delete the registration.

The application receives notifications about the ducking events through the methods of the <a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiovolumeducknotification">IAudioVolumeDuckNotification</a> interface. The application implements <b>IAudioVolumeDuckNotification</b>. After the registration call has succeeded, the system calls the methods of this interface when session events occur.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2">IAudioSessionManager2</a>



<a href="/windows/desktop/CoreAudio/using-the-communication-device">Using a Communication Device</a>