---
UID: NF:audiopolicy.IAudioSessionEvents.OnDisplayNameChanged
title: IAudioSessionEvents::OnDisplayNameChanged
author: windows-sdk-content
description: The OnDisplayNameChanged method notifies the client that the display name for the session has changed.
old-location: coreaudio\iaudiosessionevents_ondisplaynamechanged.htm
tech.root: CoreAudio
ms.assetid: 65d21f0c-b6f1-4506-975c-6d0308b3fc2f
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IAudioSessionEvents interface [Core Audio],OnDisplayNameChanged method, IAudioSessionEvents.OnDisplayNameChanged, IAudioSessionEvents::OnDisplayNameChanged, IAudioSessionEventsOnDisplayNameChanged, OnDisplayNameChanged, OnDisplayNameChanged method [Core Audio], OnDisplayNameChanged method [Core Audio],IAudioSessionEvents interface, audiopolicy/IAudioSessionEvents::OnDisplayNameChanged, coreaudio.iaudiosessionevents_ondisplaynamechanged
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
 - IAudioSessionEvents.OnDisplayNameChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioSessionEvents::OnDisplayNameChanged


## -description



The <b>OnDisplayNameChanged</b> method notifies the client that the display name for the session has changed.




## -parameters




### -param NewDisplayName [in]

The new display name for the session. This parameter points to a null-terminated, wide-character string containing the new display name. The string remains valid for the duration of the call.


### -param EventContext [in]

The event context value. This is the same value that the caller passed to <a href="https://msdn.microsoft.com/d12c12ed-a556-4743-952e-2eb4f58ee0eb">IAudioSessionControl::SetDisplayName</a> in the call that changed the display name for the session. For more information, see Remarks.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The session manager calls this method each time a call to the <a href="https://msdn.microsoft.com/d12c12ed-a556-4743-952e-2eb4f58ee0eb">IAudioSessionControl::SetDisplayName</a> method changes the display name of the session. The Sndvol program uses a session's display name to label the volume slider for the session.

The <i>EventContext</i> parameter provides a means for a client to distinguish between a display-name change that it initiated and one that some other client initiated. When calling the <a href="https://msdn.microsoft.com/d12c12ed-a556-4743-952e-2eb4f58ee0eb">IAudioSessionControl::SetDisplayName</a> method, a client passes in an <i>EventContext</i> parameter value that its implementation of the <b>OnDisplayNameChanged</b> method can recognize.

For a code example that implements the methods in the <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface, see <a href="https://msdn.microsoft.com/6943b405-0807-412b-a149-fc3a8ece1b48">Audio Session Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/d12c12ed-a556-4743-952e-2eb4f58ee0eb">IAudioSessionControl::SetDisplayName</a>



<a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents Interface</a>
 

 

