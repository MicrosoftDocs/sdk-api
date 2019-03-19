---
UID: NF:audiopolicy.IAudioSessionEvents.OnGroupingParamChanged
title: IAudioSessionEvents::OnGroupingParamChanged (audiopolicy.h)
author: windows-sdk-content
description: The OnGroupingParamChanged method notifies the client that the grouping parameter for the session has changed.
old-location: coreaudio\iaudiosessionevents_ongroupingparamchanged.htm
tech.root: CoreAudio
ms.assetid: f52c9d8a-245b-489a-81c1-cb4715faa8be
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioSessionEvents interface [Core Audio],OnGroupingParamChanged method, IAudioSessionEvents.OnGroupingParamChanged, IAudioSessionEvents::OnGroupingParamChanged, IAudioSessionEventsOnGroupingParamChanged, OnGroupingParamChanged, OnGroupingParamChanged method [Core Audio], OnGroupingParamChanged method [Core Audio],IAudioSessionEvents interface, audiopolicy/IAudioSessionEvents::OnGroupingParamChanged, coreaudio.iaudiosessionevents_ongroupingparamchanged
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
 - IAudioSessionEvents.OnGroupingParamChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioSessionEvents::OnGroupingParamChanged


## -description



The <b>OnGroupingParamChanged</b> method notifies the client that the grouping parameter for the session has changed.




## -parameters




### -param NewGroupingParam [in]

The new grouping parameter for the session. This parameter points to a grouping-parameter GUID.


### -param EventContext [in]

The event context value. This is the same value that the caller passed to <a href="https://msdn.microsoft.com/990bebd9-c37d-4f72-b349-a43a074d8992">IAudioSessionControl::SetGroupingParam</a> in the call that changed the grouping parameter for the session. For more information, see Remarks.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The session manager calls this method each time a call to the <a href="https://msdn.microsoft.com/990bebd9-c37d-4f72-b349-a43a074d8992">IAudioSessionControl::SetGroupingParam</a> method changes the grouping parameter for the session.

The <i>EventContext</i> parameter provides a means for a client to distinguish between a grouping-parameter change that it initiated and one that some other client initiated. When calling the <a href="https://msdn.microsoft.com/990bebd9-c37d-4f72-b349-a43a074d8992">IAudioSessionControl::SetGroupingParam</a> method, a client passes in an <i>EventContext</i> parameter value that its implementation of the <b>OnGroupingParamChanged</b> method can recognize.

For a code example that implements the methods in the <a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents</a> interface, see <a href="https://msdn.microsoft.com/6943b405-0807-412b-a149-fc3a8ece1b48">Audio Session Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/990bebd9-c37d-4f72-b349-a43a074d8992">IAudioSessionControl::SetGroupingParam</a>



<a href="https://msdn.microsoft.com/fd287ef7-8a37-4342-b4c2-79b84a56c30e">IAudioSessionEvents Interface</a>
 

 

