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
 

 

