---
UID: NN:rdpencomapi.IRDPSRAPIInvitation
title: IRDPSRAPIInvitation
author: windows-sdk-content
description: Invitations enable a person or group of persons to connect to a session. When an attendee connects to a session, the client sends a ticket and a password. These two pieces of information are used to authenticate an attendee.
old-location: rdp\irdpsrapiinvitation.htm
tech.root: rdp
ms.assetid: 66cd8251-726a-4368-8da5-4d3f6899bdc8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRDPSRAPIInvitation, IRDPSRAPIInvitation interface [RDP], IRDPSRAPIInvitation interface [RDP],described, rdp.irdpsrapiinvitation, rdpencomapi/IRDPSRAPIInvitation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IRDPSRAPIInvitation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPIInvitation interface


## -description


Invitations enable a person or group of persons to connect to a session. When an attendee connects to a session, the client sends a ticket and a password. These two pieces of information are used to authenticate an attendee.

Applications obtain access to this object using <a href="https://msdn.microsoft.com/169d220b-3a2a-490e-9c1c-03a707d59f6c">IRDPSRAPIInvitationManager::CreateInvitation</a>.

An attendee can join a session if the invitation list contains and invitation with the following properties:
<ul>
<li>The ticket string in <a href="https://msdn.microsoft.com/46f44927-c29e-401c-b81e-d009c1ad3c97">ConnectionString</a> matches the one sent by the client.</li>
<li>The password string in <a href="https://msdn.microsoft.com/53d55a81-73c3-4196-b23e-b4719a1ceced">Password</a> matches the one sent by the client.</li>
<li>The number of attendees has not exceeded the maximum number in <a href="https://msdn.microsoft.com/ab16039f-210a-46ba-aaa8-0dcc840123b2">AttendeeLimit</a>.</li>
<li>The invitation has not been revoked using <a href="https://msdn.microsoft.com/a5a2d1a4-a51b-4fd4-b79c-3381f296d072">Revoked</a>.</li>
</ul>

## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/300940ef-e8a6-4dd9-a078-d4325e20ae91">IRDPSRAPIInvitationManager</a>
 

 

