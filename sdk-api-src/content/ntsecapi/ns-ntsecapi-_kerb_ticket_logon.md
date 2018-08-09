---
UID: NS:ntsecapi._KERB_TICKET_LOGON
title: "_KERB_TICKET_LOGON"
author: windows-sdk-content
description: Contains profile information for a network logon.
old-location: security\kerb_ticket_logon.htm
old-project: secauthn
ms.assetid: 2c082c79-ce7f-45a1-8552-3b4e9034b7e3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PKERB_TICKET_LOGON, KERB_TICKET_LOGON, KERB_TICKET_LOGON structure [Security], PKERB_TICKET_LOGON, PKERB_TICKET_LOGON structure pointer [Security], _KERB_TICKET_LOGON, _lsa_kerb_ticket_logon, ntsecapi/KERB_TICKET_LOGON, ntsecapi/PKERB_TICKET_LOGON, security.kerb_ticket_logon"
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
req.typenames: KERB_TICKET_LOGON, *PKERB_TICKET_LOGON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_TICKET_LOGON
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _KERB_TICKET_LOGON structure


## -description


The <b>KERB_TICKET_LOGON</b> structure contains profile information for a network logon.

It is used by the 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function.


## -struct-fields




### -field MessageType


<a href="https://msdn.microsoft.com/500bee53-638b-4782-b42d-1df158396fb6">KERB_LOGON_SUBMIT_TYPE</a> value identifying the type of logon request being made. This member must be set to <b>KerbTicketLogon</b>.


### -field Flags

<b>ULONG</b> that can be set to KERB_LOGON_FLAG_ALLOW_EXPIRED_TICKET to allow a locked workstation to re-logon with expired ticket. Other values are ignored.


### -field ServiceTicketLength

Indicates the length of the <b>ServiceTicket</b> buffer.


### -field TicketGrantingTicketLength

Indicates the length of the <b>TicketGrantingTicket</b> buffer. Must be set to zero for an empty buffer.


### -field ServiceTicket

Required ticket for service "host" or the computer account <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">service principal name</a> (SPN) in the form of an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASN.1</a> encoded Kerberos ticket. Expired tickets are acceptable if the <b>Flags</b> member is set to KERB_LOGON_FLAG_ALLOW_EXPIRED_TICKET.


### -field TicketGrantingTicket

Optional buffer containing an ASN.1-encoded KRB_CRED message containing the user's Kerberos ticket-granting ticket (KRBTGT) to be used to initialize the credential cache. The ticket must have the "forwarded" flag set in the ticket options. The KRB_CRED message is defined in Section 5.8 of  Internet <a href="http://www.ietf.org/rfc/rfc4120.txt">RFC 4120</a>. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84023">http://www.ietf.org</a>.


## -remarks



The service ticket must be for the host SPN of the computer. If the ticket includes a Windows Privilege Attribute Certificate (PAC), it will be used to construct the user's logon token. Otherwise, an anonymous token will be created using the client principal name in the ticket.

If a ticket-granting ticket (TGT) is supplied as a KRB_CRED message, it is placed in the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a> credentials cache. If the TGT is omitted, the logon will be only for the local machine.



