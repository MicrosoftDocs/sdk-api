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

# IRDPSRAPIAttendee::TerminateConnection


## -description


Disconnects the client represented by the attendee.


## -parameters






## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code. The following is a possible value.




## -remarks



This method disconnects clients from the session. The clients can reconnect because the authentication is based on the invitation. To provide stricter access control to the session, an application can create one invitation object per attendee and revoke the invitation at the same time it calls this method.

This call is not blocking. However, termination is not immediate and can be delayed by a send operation. If the thread that is managing connections is in the middle of sending a buffer, it must wait for the buffer to be sent. The caller should consider the attendee disconnected only after the <a href="https://msdn.microsoft.com/4edcd497-8821-46c0-8d44-0b24e4f3f285">_IRDPSessionEvents::OnAttendeeDisconnected</a> event is fired.




## -see-also




<a href="https://msdn.microsoft.com/e9edd9f2-ccbf-45b2-b71c-e30368435a60">IRDPSRAPIAttendee</a>
 

 

