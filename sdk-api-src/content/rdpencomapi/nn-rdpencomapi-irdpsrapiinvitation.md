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

# IRDPSRAPIInvitation interface


## -description


Invitations enable a person or group of persons to connect to a session. When an attendee connects to a session, the client sends a ticket and a password. These two pieces of information are used to authenticate an attendee.

Applications obtain access to this object using <a href="https://msdn.microsoft.com/169d220b-3a2a-490e-9c1c-03a707d59f6c">IRDPSRAPIInvitationManager::CreateInvitation</a>.

An attendee can join a session if the invitation list contains and invitation with the following properties:
<ul>
<li>The ticket string in <a href="https://msdn.microsoft.com/46f44927-c29e-401c-b81e-d009c1ad3c97">ConnectionString</a> matches the one sent by the client.</li>
<li>The password string in <a href="https://msdn.microsoft.com/library/windows/hardware/dn915695">Password</a> matches the one sent by the client.</li>
<li>The number of attendees has not exceeded the maximum number in <a href="https://msdn.microsoft.com/ab16039f-210a-46ba-aaa8-0dcc840123b2">AttendeeLimit</a>.</li>
<li>The invitation has not been revoked using <a href="https://msdn.microsoft.com/a5a2d1a4-a51b-4fd4-b79c-3381f296d072">Revoked</a>.</li>
</ul>

## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/300940ef-e8a6-4dd9-a078-d4325e20ae91">IRDPSRAPIInvitationManager</a>
 

 

