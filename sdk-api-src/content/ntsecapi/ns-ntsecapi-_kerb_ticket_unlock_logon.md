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

# _KERB_TICKET_UNLOCK_LOGON structure


## -description


The <b>KERB_TICKET_UNLOCK_LOGON</b> structure contains information to unlock a workstation.

It is used by 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>.


## -struct-fields




### -field Logon


<a href="https://msdn.microsoft.com/2c082c79-ce7f-45a1-8552-3b4e9034b7e3">KERB_TICKET_LOGON</a> structure. All members of the structure must be the same as the structure used in the original logon except the <a href="https://msdn.microsoft.com/500bee53-638b-4782-b42d-1df158396fb6">KERB_LOGON_SUBMIT_TYPE</a> member, which must be set to <b>KerbTicketUnlockLogon</b>.


### -field LogonId


<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> structure containing the logon identifier of the current <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>. This ID was previously returned from the initial logon by 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>.

