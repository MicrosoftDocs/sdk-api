---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

