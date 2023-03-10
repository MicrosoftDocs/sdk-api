---
UID: NF:rdpencomapi.IRDPSRAPIAttendee.TerminateConnection
title: IRDPSRAPIAttendee::TerminateConnection (rdpencomapi.h)
description: Disconnects the client represented by the attendee.
helpviewer_keywords: ["IRDPSRAPIAttendee interface [RDP]","TerminateConnection method","IRDPSRAPIAttendee.TerminateConnection","IRDPSRAPIAttendee::TerminateConnection","TerminateConnection","TerminateConnection method [RDP]","TerminateConnection method [RDP]","IRDPSRAPIAttendee interface","rdp.irdpsrapiattendee_terminateconnection","rdpencomapi/IRDPSRAPIAttendee::TerminateConnection"]
old-location: rdp\irdpsrapiattendee_terminateconnection.htm
tech.root: rdp
ms.assetid: e666fdd4-7417-40ea-9643-d7df587294f2
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIAttendee interface [RDP],TerminateConnection method, IRDPSRAPIAttendee.TerminateConnection, IRDPSRAPIAttendee::TerminateConnection, TerminateConnection, TerminateConnection method [RDP], TerminateConnection method [RDP],IRDPSRAPIAttendee interface, rdp.irdpsrapiattendee_terminateconnection, rdpencomapi/IRDPSRAPIAttendee::TerminateConnection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPIAttendee::TerminateConnection
 - rdpencomapi/IRDPSRAPIAttendee::TerminateConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIAttendee.TerminateConnection
---

# IRDPSRAPIAttendee::TerminateConnection


## -description

Disconnects the client represented by the attendee.



## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code. The following is a possible value.

## -remarks

This method disconnects clients from the session. The clients can reconnect because the authentication is based on the invitation. To provide stricter access control to the session, an application can create one invitation object per attendee and revoke the invitation at the same time it calls this method.

This call is not blocking. However, termination is not immediate and can be delayed by a send operation. If the thread that is managing connections is in the middle of sending a buffer, it must wait for the buffer to be sent. The caller should consider the attendee disconnected only after the <a href="/previous-versions/windows/desktop/rdp/onattendeedisconnected">_IRDPSessionEvents::OnAttendeeDisconnected</a> event is fired.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiattendee">IRDPSRAPIAttendee</a>
