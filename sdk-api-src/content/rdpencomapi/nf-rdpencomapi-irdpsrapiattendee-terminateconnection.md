---
UID: NF:rdpencomapi.IRDPSRAPIAttendee.TerminateConnection
title: IRDPSRAPIAttendee::TerminateConnection (rdpencomapi.h)
author: windows-sdk-content
description: Disconnects the client represented by the attendee.
old-location: rdp\irdpsrapiattendee_terminateconnection.htm
tech.root: rdp
ms.assetid: e666fdd4-7417-40ea-9643-d7df587294f2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIAttendee interface [RDP],TerminateConnection method, IRDPSRAPIAttendee.TerminateConnection, IRDPSRAPIAttendee::TerminateConnection, TerminateConnection, TerminateConnection method [RDP], TerminateConnection method [RDP],IRDPSRAPIAttendee interface, rdp.irdpsrapiattendee_terminateconnection, rdpencomapi/IRDPSRAPIAttendee::TerminateConnection
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIAttendee.TerminateConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

