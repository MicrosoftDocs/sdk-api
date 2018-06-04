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

# _AudioSessionState enumeration


## -description



The <b>AudioSessionState</b> enumeration defines constants that indicate the current state of an audio session.




## -enum-fields




### -field AudioSessionStateInactive

The audio session is inactive. (It contains at least one stream, but none of the streams in the session is currently running.)


### -field AudioSessionStateActive

The audio session is active. (At least one of the streams in the session is running.)


### -field AudioSessionStateExpired

The audio session has expired. (It contains no streams.)


## -remarks



When a client opens a session by assigning the first stream to the session (by calling the <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> method), the initial session state is inactive. The session state changes from inactive to active when a stream in the session begins running (because the client has called the <a href="https://msdn.microsoft.com/706f9833-7f06-4bdc-96d5-6872f6effcb9">IAudioClient::Start</a> method). The session changes from active to inactive when the client stops the last running stream in the session (by calling the <a href="https://msdn.microsoft.com/d5824aa9-0b91-4bee-9c0c-26e12a6b96b5">IAudioClient::Stop</a> method). The session state changes to expired when the client destroys the last stream in the session by releasing all references to the stream object.

The system volume-control program, Sndvol, displays volume controls for both active and inactive sessions. Sndvol stops displaying the volume control for a session when the session state changes to expired. For more information about Sndvol, see <a href="https://msdn.microsoft.com/b8a1b656-a582-4112-99e9-bd575719ebb3">Audio Sessions</a>.

The <a href="https://msdn.microsoft.com/9c0188a1-7982-40f0-9040-bda00473160c">IAudioSessionControl::GetState</a> and <a href="https://msdn.microsoft.com/4ec3e676-cf08-4041-b5bf-5cb429569e03">IAudioSessionEvents::OnStateChanged</a> methods use the constants defined in the <b>AudioSessionState</b> enumeration.

For more information about session states, see <a href="https://msdn.microsoft.com/b8a1b656-a582-4112-99e9-bd575719ebb3">Audio Sessions</a>.




## -see-also




<a href="https://msdn.microsoft.com/9dc9f182-3adf-4171-8829-35debae123da">Core Audio Constants</a>



<a href="https://msdn.microsoft.com/7d25be71-ffbe-4e8c-9a45-cdeb35d10292">Core Audio Enumerations</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>



<a href="https://msdn.microsoft.com/706f9833-7f06-4bdc-96d5-6872f6effcb9">IAudioClient::Start</a>



<a href="https://msdn.microsoft.com/d5824aa9-0b91-4bee-9c0c-26e12a6b96b5">IAudioClient::Stop</a>



<a href="https://msdn.microsoft.com/9c0188a1-7982-40f0-9040-bda00473160c">IAudioSessionControl::GetState</a>



<a href="https://msdn.microsoft.com/4ec3e676-cf08-4041-b5bf-5cb429569e03">IAudioSessionEvents::OnStateChanged</a>
 

 

