---
UID: NF:audiopolicy.IAudioSessionControl.UnregisterAudioSessionNotification
title: IAudioSessionControl::UnregisterAudioSessionNotification
author: windows-sdk-content
description: The UnregisterAudioSessionNotification method deletes a previous registration by the client to receive notifications.
old-location: coreaudio\iaudiosessioncontrol_unregisteraudiosessionnotification.htm
old-project: CoreAudio
ms.assetid: 1b496d58-c855-44b8-b437-6cb6017dcc9d
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IAudioSessionControl interface [Core Audio],UnregisterAudioSessionNotification method, IAudioSessionControl.UnregisterAudioSessionNotification, IAudioSessionControl::UnregisterAudioSessionNotification, IAudioSessionControlUnregisterAudioSessionNotification, UnregisterAudioSessionNotification, UnregisterAudioSessionNotification method [Core Audio], UnregisterAudioSessionNotification method [Core Audio],IAudioSessionControl interface, audiopolicy/IAudioSessionControl::UnregisterAudioSessionNotification, coreaudio.iaudiosessioncontrol_unregisteraudiosessionnotification
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UNCOMPRESSEDAUDIOFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audiopolicy.h
api_name:
 - IAudioSessionControl.UnregisterAudioSessionNotification
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSessionControl::UnregisterAudioSessionNotification


## -description



The <b>UnregisterAudioSessionNotification</b> method deletes a previous registration by the client to receive notifications.




## -parameters




### -param NewNotifications [in]

Pointer to a client-implemented <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface. The client passed this same interface pointer to the session manager in a previous call to the <a href="https://msdn.microsoft.com/f0004eb6-1b3c-4f78-9ab4-17b30dec0d94">IAudioSessionControl::RegisterAudioSessionNotification</a> method. If the <b>UnregisterAudioSessionNotification</b> method succeeds, it calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method on the client's <b>IAudioSessionEvents</b> interface.


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
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified interface was not previously registered by the client or has already been removed.

</td>
</tr>
</table>
 




## -remarks



The client calls this method when it no longer needs to receive notifications. The <b>UnregisterAudioSessionNotification</b> method removes the registration of an <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface that the client previously registered with the session manager by calling the <a href="https://msdn.microsoft.com/f0004eb6-1b3c-4f78-9ab4-17b30dec0d94">IAudioSessionControl::RegisterAudioSessionNotification</a> method.

Before the client releases its final reference to the <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface, it should call <b>UnregisterAudioSessionNotification</b> to unregister the interface. Otherwise, the application leaks the resources held by the <b>IAudioSessionEvents</b> and <a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl</a> objects. Note that <a href="https://msdn.microsoft.com/f0004eb6-1b3c-4f78-9ab4-17b30dec0d94">RegisterAudioSessionNotification</a> calls the client's <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IAudioSessionEvents::AddRef</a> method, and <b>UnregisterAudioSessionNotification</b> calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IAudioSessionEvents::Release</a> method. If the client errs by releasing its reference to the <b>IAudioSessionEvents</b> interface before calling <b>UnregisterAudioSessionNotification</b>, the session manager never releases its reference to the <b>IAudioSessionEvents</b> interface. For example, a poorly designed <b>IAudioSessionEvents</b> implementation might call <b>UnregisterAudioSessionNotification</b> from the destructor for the <b>IAudioSessionEvents</b> object. In this case, the client will not call <b>UnregisterAudioSessionNotification</b> until the session manager releases its reference to the <b>IAudioSessionEvents</b> interface, and the session manager will not release its reference to the <b>IAudioSessionEvents</b> interface until the client calls <b>UnregisterAudioSessionNotification</b>. For more information about the <b>AddRef</b> and <b>Release</b> methods, see the discussion of the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface in the Windows SDK documentation.

For a code example that calls the <b>UnregisterAudioSessionNotification</b> method, see <a href="https://msdn.microsoft.com/91a93b79-2563-4b25-af5d-ca5f7d35d77b">Audio Events for Legacy Audio Applications</a>.




## -see-also




<a href="https://msdn.microsoft.com/4446140e-2e61-40ed-b0f9-4c1b90e7c2de">IAudioSessionControl Interface</a>



<a href="https://msdn.microsoft.com/f0004eb6-1b3c-4f78-9ab4-17b30dec0d94">IAudioSessionControl::RegisterAudioSessionNotification</a>



<a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents Interface</a>
 

 

