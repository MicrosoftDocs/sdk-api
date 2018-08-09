---
UID: NF:audiopolicy.IAudioSessionManager2.RegisterSessionNotification
title: IAudioSessionManager2::RegisterSessionNotification
author: windows-sdk-content
description: The RegisterSessionNotification method registers the application to receive a notification when a session is created.
old-location: coreaudio\iaudiosessionmanager2_registersessionnotification.htm
old-project: CoreAudio
ms.assetid: cff43da7-70b2-4887-8a6c-6100cf7d696e
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IAudioSessionManager2 interface [Core Audio],RegisterSessionNotification method, IAudioSessionManager2.RegisterSessionNotification, IAudioSessionManager2::RegisterSessionNotification, RegisterSessionNotification, RegisterSessionNotification method [Core Audio], RegisterSessionNotification method [Core Audio],IAudioSessionManager2 interface, audiopolicy/IAudioSessionManager2::RegisterSessionNotification, coreaudio.iaudiosessionmanager2_registersessionnotification
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UNCOMPRESSEDAUDIOFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiopolicy.h
api_name:
 - IAudioSessionManager2.RegisterSessionNotification
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSessionManager2::RegisterSessionNotification


## -description


The <b>RegisterSessionNotification</b> method registers the application to receive a notification when a session is created.


## -parameters




### -param SessionNotification

A pointer to the application's implementation of the <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> interface. If the method call succeeds, it calls the <b>AddRef</b> method on the application's <b>IAudioSessionNotification</b> interface.



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



The application can register to receive a notification  when a session is created, through the methods  of the <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> interface.  The application implements the <b>IAudioSessionNotification</b> interface. The methods defined in this interface receive callbacks from the  system when a session is created. For example code that shows how to implement this interface, see 

<a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification Interface</a>.

To begin receiving notifications, the application calls the <b>IAudioSessionManager2::RegisterSessionNotification</b> method to register its <a href="https://msdn.microsoft.com/69222168-87d7-4f5a-93b1-6d91263a54bd">IAudioSessionNotification</a> interface. When the application no longer requires notifications, it calls the <a href="https://msdn.microsoft.com/0c334963-2b60-4eb1-b8a2-c9ed0d21bd5e">IAudioSessionManager2::UnregisterSessionNotification</a> method to delete the registration.

<div class="alert"><b>Note</b>  Make sure that the application initializes COM with Multithreaded Apartment (MTA) model by calling <code>CoInitializeEx(NULL, COINIT_MULTITHREADED)</code> in a non-UI thread. If MTA is not initialized, the application does not receive session notifications from the session manager. 
Threads that run the user interface of an application should be initialized apartment threading model.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/476dac90-d0c4-499c-973e-33ea55546659">IAudioSessionManager2</a>
 

 

