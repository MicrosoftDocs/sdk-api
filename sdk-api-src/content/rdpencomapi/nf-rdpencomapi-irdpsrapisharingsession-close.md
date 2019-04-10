---
UID: NF:rdpencomapi.IRDPSRAPISharingSession.Close
title: IRDPSRAPISharingSession::Close (rdpencomapi.h)
author: windows-sdk-content
description: Disconnects all attendees from the session and stops listening to incoming connections.
old-location: rdp\irdpsrapisharingsession_close.htm
tech.root: rdp
ms.assetid: ab6e27d8-b6f2-42a6-a0f6-cfdfb5ec9a13
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Close, Close method [RDP], Close method [RDP],IRDPSRAPISharingSession interface, Close method [RDP],IRDPSRAPISharingSession2 interface, IRDPSRAPISharingSession interface [RDP],Close method, IRDPSRAPISharingSession.Close, IRDPSRAPISharingSession2 interface [RDP],Close method, IRDPSRAPISharingSession2::Close, IRDPSRAPISharingSession::Close, rdp.irdpsrapisharingsession_close, rdpencomapi/IRDPSRAPISharingSession2::Close, rdpencomapi/IRDPSRAPISharingSession::Close
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - IRDPSRAPISharingSession2.Close
 - IRDPSRAPISharingSession.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPISharingSession::Close


## -description


Disconnects all  attendees from the session and stops listening to incoming connections.

When the attendees are disconnected, no attendee disconnect event occurs on the sharer side because it is the sharer that calls this method.  The sharer is already aware that the attendees will be disconnected.

A closed session cannot be reopened by calling the <a href="https://msdn.microsoft.com/2c97a37d-5862-4ad3-9029-481ea0a789e0">IRDPSRAPISharingSession::Open</a> method.


## -parameters






## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/531382ec-d94f-411e-bd43-86cd3066ac26">IRDPSRAPISharingSession</a>



<a href="https://msdn.microsoft.com/3ac68be7-e6fd-42c7-b2f3-b90bb5097b07">IRDPSRAPISharingSession2</a>
 

 

