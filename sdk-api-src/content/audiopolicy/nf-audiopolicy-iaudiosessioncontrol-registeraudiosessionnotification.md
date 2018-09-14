---
UID: NF:audiopolicy.IAudioSessionControl.RegisterAudioSessionNotification
title: IAudioSessionControl::RegisterAudioSessionNotification
author: windows-sdk-content
description: The RegisterAudioSessionNotification method registers the client to receive notifications of session events, including changes in the stream state.
old-location: coreaudio\iaudiosessioncontrol_registeraudiosessionnotification.htm
tech.root: CoreAudio
ms.assetid: f0004eb6-1b3c-4f78-9ab4-17b30dec0d94
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAudioSessionControl interface [Core Audio],RegisterAudioSessionNotification method, IAudioSessionControl.RegisterAudioSessionNotification, IAudioSessionControl::RegisterAudioSessionNotification, IAudioSessionControlRegisterAudioSessionNotification, RegisterAudioSessionNotification, RegisterAudioSessionNotification method [Core Audio], RegisterAudioSessionNotification method [Core Audio],IAudioSessionControl interface, audiopolicy/IAudioSessionControl::RegisterAudioSessionNotification, coreaudio.iaudiosessioncontrol_registeraudiosessionnotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audiopolicy.h
api_name:
 - IAudioSessionControl.RegisterAudioSessionNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioSessionControl::RegisterAudioSessionNotification


## -description



The <b>RegisterAudioSessionNotification</b> method registers the client to receive notifications of session events, including changes in the stream state.




## -parameters




### -param NewNotifications [in]

Pointer to a client-implemented <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface. If the method succeeds, it calls the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method on the client's <b>IAudioSessionEvents</b> interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>NewNotifications</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>
 




## -remarks



This method passes a client-implemented <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface to the session manager. Following a successful call to this method, the session manager calls the methods in the <b>IAudioSessionEvents</b> interface to notify the client of various session events. Through these methods, the client receives notifications of the following session-related events:

<ul>
<li>Display name changes</li>
<li>Volume level changes</li>
<li>Session state changes (inactive to active, or active to inactive)</li>
<li>Grouping parameter changes</li>
<li>Disconnection of the client from the session (caused by the user removing the audio endpoint device, shutting down the session manager, or changing the stream format)</li>
</ul>
When notifications are no longer needed, the client can call the <a href="https://msdn.microsoft.com/1b496d58-c855-44b8-b437-6cb6017dcc9d">IAudioSessionControl::UnregisterAudioSessionNotification</a> method to terminate the notifications.

Before the client releases its final reference to the <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface, it should call <a href="https://msdn.microsoft.com/1b496d58-c855-44b8-b437-6cb6017dcc9d">UnregisterAudioSessionNotification</a> to unregister the interface. Otherwise, the application leaks the resources held by the <b>IAudioSessionEvents</b> and <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> objects. Note that <b>RegisterAudioSessionNotification</b> calls the client's <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IAudioSessionEvents::AddRef</a> method, and <b>UnregisterAudioSessionNotification</b> calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IAudioSessionEvents::Release</a> method. If the client errs by releasing its reference to the <b>IAudioSessionEvents</b> interface before calling <b>UnregisterAudioSessionNotification</b>, the session manager never releases its reference to the <b>IAudioSessionEvents</b> interface. For example, a poorly designed <b>IAudioSessionEvents</b> implementation might call <b>UnregisterAudioSessionNotification</b> from the destructor for the <b>IAudioSessionEvents</b> object. In this case, the client will not call <b>UnregisterAudioSessionNotification</b> until the session manager releases its reference to the <b>IAudioSessionEvents</b> interface, and the session manager will not release its reference to the <b>IAudioSessionEvents</b> interface until the client calls <b>UnregisterAudioSessionNotification</b>. For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface in the Windows SDK documentation.

In addition, the client should call <a href="https://msdn.microsoft.com/1b496d58-c855-44b8-b437-6cb6017dcc9d">UnregisterAudioSessionNotification</a> before releasing all of its references to the <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> and <a href="https://msdn.microsoft.com/606b0a42-d1d1-4196-911f-5b095bf56c4e">IAudioSessionManager</a> objects. Unless the client retains a reference to at least one of these two objects, the session manager leaks the storage that it allocated to hold the registration information. After registering a notification interface, the client continues to receive notifications for only as long as at least one of these two objects exists.

For a code example that calls the <b>RegisterAudioSessionNotification</b> method, see <a href="https://msdn.microsoft.com/91a93b79-2563-4b25-af5d-ca5f7d35d77b">Audio Events for Legacy Audio Applications</a>.




## -see-also




<a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl Interface</a>



<a href="https://msdn.microsoft.com/1b496d58-c855-44b8-b437-6cb6017dcc9d">IAudioSessionControl::UnregisterAudioSessionNotification</a>



<a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents Interface</a>



<a href="https://msdn.microsoft.com/606b0a42-d1d1-4196-911f-5b095bf56c4e">IAudioSessionManager</a>
 

 

