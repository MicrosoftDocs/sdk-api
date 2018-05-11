---
UID: NF:audiopolicy.IAudioSessionEvents.OnSessionDisconnected
title: IAudioSessionEvents::OnSessionDisconnected
author: windows-driver-content
description: The OnSessionDisconnected method notifies the client that the audio session has been disconnected.
old-location: coreaudio\iaudiosessionevents_onsessiondisconnected.htm
old-project: CoreAudio
ms.assetid: 9fd653f0-c9d1-4155-9c1e-7e6124b40cca
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IAudioSessionEvents interface [Core Audio],OnSessionDisconnected method, IAudioSessionEvents.OnSessionDisconnected, IAudioSessionEvents::OnSessionDisconnected, IAudioSessionEventsOnSessionDisconnected, OnSessionDisconnected, OnSessionDisconnected method [Core Audio], OnSessionDisconnected method [Core Audio],IAudioSessionEvents interface, audiopolicy/IAudioSessionEvents::OnSessionDisconnected, coreaudio.iaudiosessionevents_onsessiondisconnected
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
-	Audiopolicy.h
api_name:
-	IAudioSessionEvents.OnSessionDisconnected
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSessionEvents::OnSessionDisconnected


## -description



The <b>OnSessionDisconnected</b> method notifies the client that the audio session has been disconnected.




## -parameters




### -param DisconnectReason [in]

The reason that the audio session was disconnected. The caller sets this parameter to one of the <b>AudioSessionDisconnectReason</b> enumeration values shown in the following table.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>DisconnectReasonDeviceRemoval</td>
<td>The user removed the audio endpoint device.</td>
</tr>
<tr>
<td>DisconnectReasonServerShutdown</td>
<td>The Windows audio service has stopped.</td>
</tr>
<tr>
<td>DisconnectReasonFormatChanged</td>
<td>The stream format changed for the device that the audio session is connected to.</td>
</tr>
<tr>
<td>DisconnectReasonSessionLogoff</td>
<td>The user logged off the Windows Terminal Services (WTS) session that the audio session was running in.</td>
</tr>
<tr>
<td>DisconnectReasonSessionDisconnected</td>
<td>The WTS session that the audio session was running in was disconnected.</td>
</tr>
<tr>
<td>DisconnectReasonExclusiveModeOverride</td>
<td>The (shared-mode) audio session was disconnected to make the audio endpoint device available for an exclusive-mode connection.</td>
</tr>
</table>
 

For more information about WTS sessions, see the Windows SDK documentation.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



When disconnecting a session, the session manager closes the streams that belong to that session and invalidates all outstanding requests for services on those streams. The client should respond to a disconnection by releasing all of its references to the <a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a> interface for a closed stream and releasing all references to the service interfaces that it obtained previously through calls to the <a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a> method.

Following disconnection, many of the methods in the WASAPI interfaces that are tied to closed streams in the disconnected session return error code AUDCLNT_E_DEVICE_INVALIDATED (for example, see <a href="https://msdn.microsoft.com/2a2c9ddf-f668-41ff-85f0-34de593c0fe2">IAudioClient::GetCurrentPadding</a>). For information about recovering from this error, see <a href="https://msdn.microsoft.com/1f5c3458-70ca-45ba-ac33-5c7b9f092320">Recovering from an Invalid-Device Error</a>.

If the Windows audio service terminates unexpectedly, it does not have an opportunity to notify clients that it is shutting down. In that case, clients learn that the service has stopped when they call a method such as <a href="https://msdn.microsoft.com/2a2c9ddf-f668-41ff-85f0-34de593c0fe2">IAudioClient::GetCurrentPadding</a> that discovers that the service is no longer running and fails with error code AUDCLNT_E_SERVICE_NOT_RUNNING.

A client cannot generate a session-disconnected event. The system is always the source of this type of event. Thus, unlike some other <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> methods, this method does not have a context parameter.

For a code example that implements the methods in the <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface, see <a href="https://msdn.microsoft.com/6943b405-0807-412b-a149-fc3a8ece1b48">Audio Session Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient Interface</a>



<a href="https://msdn.microsoft.com/233d4471-037f-4df9-bef6-57f2544dedb5">IAudioClient::GetService</a>



<a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents Interface</a>
 

 

