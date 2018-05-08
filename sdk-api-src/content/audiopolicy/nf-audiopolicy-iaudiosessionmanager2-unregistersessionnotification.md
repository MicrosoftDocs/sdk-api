---
UID: NF:audiopolicy.IAudioSessionManager2.UnregisterSessionNotification
title: IAudioSessionManager2::UnregisterSessionNotification
author: windows-driver-content
description: The UnregisterSessionNotification method deletes the registration to receive a notification when a session is created.
old-location: coreaudio\iaudiosessionmanager2_unregistersessionnotification.htm
old-project: CoreAudio
ms.assetid: 0c334963-2b60-4eb1-b8a2-c9ed0d21bd5e
ms.author: windowsdriverdev
ms.date: 4/4/2018
ms.keywords: IAudioSessionManager2 interface [Core Audio],UnregisterSessionNotification method, IAudioSessionManager2.UnregisterSessionNotification, IAudioSessionManager2::UnregisterSessionNotification, UnregisterSessionNotification, UnregisterSessionNotification method [Core Audio], UnregisterSessionNotification method [Core Audio],IAudioSessionManager2 interface, audiopolicy/IAudioSessionManager2::UnregisterSessionNotification, coreaudio.iaudiosessionmanager2_unregistersessionnotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: UNCOMPRESSEDAUDIOFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	audiopolicy.h
api_name:
-	IAudioSessionManager2.UnregisterSessionNotification
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSessionManager2::UnregisterSessionNotification


## -description


The <b>UnregisterSessionNotification</b> method deletes the registration to  receive a notification when a session is created.


## -parameters




### -param SessionNotification

A pointer to the application's implementation of the <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> interface. Pass the same interface pointer that was specified to the session manager in  a previous call to <a href="https://msdn.microsoft.com/cff43da7-70b2-4887-8a6c-6100cf7d696e">IAudioSessionManager2::RegisterSessionNotification</a> to register for notification.  

If the <b>UnregisterSessionNotification</b> method succeeds, it calls the <b>Release</b> method on the application's <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> interface.



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



The application calls this method when it no longer needs to receive notifications. The <b>UnregisterSessionNotification</b> method removes the registration of an <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> interface that the application previously registered with the session manager by calling the <a href="https://msdn.microsoft.com/f0004eb6-1b3c-4f78-9ab4-17b30dec0d94">IAudioSessionControl::RegisterAudioSessionNotification</a> method.






## -see-also




<a href="https://msdn.microsoft.com/476dac90-d0c4-499c-973e-33ea55546659">IAudioSessionManager2</a>
 

 

