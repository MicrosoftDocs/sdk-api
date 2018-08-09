---
UID: NS:ntsecapi._KERB_TICKET_UNLOCK_LOGON
title: "_KERB_TICKET_UNLOCK_LOGON"
author: windows-sdk-content
description: Contains information to unlock a workstation.
old-location: security\kerb_ticket_unlock_logon.htm
old-project: secauthn
ms.assetid: 24daa3d1-1116-4b0b-a19b-a23075a69197
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PKERB_TICKET_UNLOCK_LOGON, KERB_TICKET_UNLOCK_LOGON, KERB_TICKET_UNLOCK_LOGON structure [Security], PKERB_TICKET_UNLOCK_LOGON, PKERB_TICKET_UNLOCK_LOGON structure pointer [Security], _KERB_TICKET_UNLOCK_LOGON, _lsa_kerb_ticket_unlock_logon, ntsecapi/KERB_TICKET_UNLOCK_LOGON, ntsecapi/PKERB_TICKET_UNLOCK_LOGON, security.kerb_ticket_unlock_logon"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: KERB_TICKET_UNLOCK_LOGON, *PKERB_TICKET_UNLOCK_LOGON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_TICKET_UNLOCK_LOGON
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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

