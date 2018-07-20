---
UID: NF:audiopolicy.IAudioSessionEvents.OnStateChanged
title: IAudioSessionEvents::OnStateChanged
author: windows-sdk-content
description: The OnStateChanged method notifies the client that the stream-activity state of the session has changed.
old-location: coreaudio\iaudiosessionevents_onstatechanged.htm
old-project: CoreAudio
ms.assetid: 4ec3e676-cf08-4041-b5bf-5cb429569e03
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: IAudioSessionEvents interface [Core Audio],OnStateChanged method, IAudioSessionEvents.OnStateChanged, IAudioSessionEvents::OnStateChanged, IAudioSessionEventsOnStateChanged, OnStateChanged, OnStateChanged method [Core Audio], OnStateChanged method [Core Audio],IAudioSessionEvents interface, audiopolicy/IAudioSessionEvents::OnStateChanged, coreaudio.iaudiosessionevents_onstatechanged
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
 - IAudioSessionEvents.OnStateChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSessionEvents::OnStateChanged


## -description



The <b>OnStateChanged</b> method notifies the client that the stream-activity state of the session has changed.




## -parameters




### -param NewState [in]

The new session state. The value of this parameter is one of the following <a href="https://msdn.microsoft.com/a972fed6-425f-46c8-b0cc-6538460bb104">AudioSessionState</a> enumeration values:

AudioSessionStateActive

AudioSessionStateInactive

AudioSessionStateExpired


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



A client cannot generate a session-state-change event. The system is always the source of this type of event. Thus, unlike some other <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> methods, this method does not supply a context parameter.

The system changes the state of a session from inactive to active at the time that a client opens the first stream in the session. A client opens a stream by calling the <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> method. The system changes the session state from active to inactive at the time that a client closes the last stream in the session. The client that releases the last reference to an <a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a> object closes the stream that is associated with the object.

For a code example that implements the methods in the <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface, see <a href="https://msdn.microsoft.com/6943b405-0807-412b-a149-fc3a8ece1b48">Audio Session Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient Interface</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>



<a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents Interface</a>
 

 

