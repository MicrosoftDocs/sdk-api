---
UID: NF:rdpencomapi.IRDPSRAPISharingSession.Close
title: IRDPSRAPISharingSession::Close (rdpencomapi.h)
description: Disconnects all attendees from the session and stops listening to incoming connections.
helpviewer_keywords: ["Close","Close method [RDP]","Close method [RDP]","IRDPSRAPISharingSession interface","Close method [RDP]","IRDPSRAPISharingSession2 interface","IRDPSRAPISharingSession interface [RDP]","Close method","IRDPSRAPISharingSession.Close","IRDPSRAPISharingSession2 interface [RDP]","Close method","IRDPSRAPISharingSession2::Close","IRDPSRAPISharingSession::Close","rdp.irdpsrapisharingsession_close","rdpencomapi/IRDPSRAPISharingSession2::Close","rdpencomapi/IRDPSRAPISharingSession::Close"]
old-location: rdp\irdpsrapisharingsession_close.htm
tech.root: rdp
ms.assetid: ab6e27d8-b6f2-42a6-a0f6-cfdfb5ec9a13
ms.date: 12/05/2018
ms.keywords: Close, Close method [RDP], Close method [RDP],IRDPSRAPISharingSession interface, Close method [RDP],IRDPSRAPISharingSession2 interface, IRDPSRAPISharingSession interface [RDP],Close method, IRDPSRAPISharingSession.Close, IRDPSRAPISharingSession2 interface [RDP],Close method, IRDPSRAPISharingSession2::Close, IRDPSRAPISharingSession::Close, rdp.irdpsrapisharingsession_close, rdpencomapi/IRDPSRAPISharingSession2::Close, rdpencomapi/IRDPSRAPISharingSession::Close
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPISharingSession::Close
 - rdpencomapi/IRDPSRAPISharingSession::Close
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
 - IRDPSRAPISharingSession2.Close
 - IRDPSRAPISharingSession.Close
---

# IRDPSRAPISharingSession::Close


## -description

Disconnects all  attendees from the session and stops listening to incoming connections.

When the attendees are disconnected, no attendee disconnect event occurs on the sharer side because it is the sharer that calls this method.  The sharer is already aware that the attendees will be disconnected.

A closed session cannot be reopened by calling the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-open">IRDPSRAPISharingSession::Open</a> method.



## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession">IRDPSRAPISharingSession</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a>
