---
UID: NF:audiopolicy.IAudioSessionEvents.OnIconPathChanged
title: IAudioSessionEvents::OnIconPathChanged
author: windows-sdk-content
description: The OnIconPathChanged method notifies the client that the display icon for the session has changed.
old-location: coreaudio\iaudiosessionevents_oniconpathchanged.htm
tech.root: CoreAudio
ms.assetid: 32669e52-28bf-4739-9f39-6e0175ca779c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioSessionEvents interface [Core Audio],OnIconPathChanged method, IAudioSessionEvents.OnIconPathChanged, IAudioSessionEvents::OnIconPathChanged, IAudioSessionEventsOnIconPathChanged, OnIconPathChanged, OnIconPathChanged method [Core Audio], OnIconPathChanged method [Core Audio],IAudioSessionEvents interface, audiopolicy/IAudioSessionEvents::OnIconPathChanged, coreaudio.iaudiosessionevents_oniconpathchanged
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
 - IAudioSessionEvents.OnIconPathChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioSessionEvents::OnIconPathChanged


## -description



The <b>OnIconPathChanged</b> method notifies the client that the display icon for the session has changed.




## -parameters




### -param NewIconPath [in]

The path for the new display icon for the session. This parameter points to a string that contains the path for the new icon. The string pointer remains valid only for the duration of the call.


### -param EventContext [in]

The event context value. This is the same value that the caller passed to <a href="https://msdn.microsoft.com/25b27a65-7204-4a12-ae4e-ad216a22e4e1">IAudioSessionControl::SetIconPath</a> in the call that changed the display icon for the session. For more information, see Remarks.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The session manager calls this method each time a call to the <a href="https://msdn.microsoft.com/25b27a65-7204-4a12-ae4e-ad216a22e4e1">IAudioSessionControl::SetIconPath</a> method changes the display icon for the session. The Sndvol program uses a session's display icon to label the volume slider for the session.

The <i>EventContext</i> parameter provides a means for a client to distinguish between a display-icon change that it initiated and one that some other client initiated. When calling the <a href="https://msdn.microsoft.com/25b27a65-7204-4a12-ae4e-ad216a22e4e1">IAudioSessionControl::SetIconPath</a> method, a client passes in an <i>EventContext</i> parameter value that its implementation of the <b>OnIconPathChanged</b> method can recognize.

For a code example that implements the methods in the <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface, see <a href="https://msdn.microsoft.com/6943b405-0807-412b-a149-fc3a8ece1b48">Audio Session Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/25b27a65-7204-4a12-ae4e-ad216a22e4e1">IAudioSessionControl::SetIconPath</a>



<a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents Interface</a>
 

 

