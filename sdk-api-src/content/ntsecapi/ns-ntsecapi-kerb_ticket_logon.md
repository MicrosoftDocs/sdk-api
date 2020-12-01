---
UID: NS:ntsecapi._KERB_TICKET_LOGON
title: KERB_TICKET_LOGON (ntsecapi.h)
description: Contains profile information for a network logon.
helpviewer_keywords: ["*PKERB_TICKET_LOGON","KERB_TICKET_LOGON","KERB_TICKET_LOGON structure [Security]","PKERB_TICKET_LOGON","PKERB_TICKET_LOGON structure pointer [Security]","_lsa_kerb_ticket_logon","ntsecapi/KERB_TICKET_LOGON","ntsecapi/PKERB_TICKET_LOGON","security.kerb_ticket_logon"]
old-location: security\kerb_ticket_logon.htm
tech.root: security
ms.assetid: 2c082c79-ce7f-45a1-8552-3b4e9034b7e3
ms.date: 12/05/2018
ms.keywords: '*PKERB_TICKET_LOGON, KERB_TICKET_LOGON, KERB_TICKET_LOGON structure [Security], PKERB_TICKET_LOGON, PKERB_TICKET_LOGON structure pointer [Security], _lsa_kerb_ticket_logon, ntsecapi/KERB_TICKET_LOGON, ntsecapi/PKERB_TICKET_LOGON, security.kerb_ticket_logon'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: KERB_TICKET_LOGON, *PKERB_TICKET_LOGON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_TICKET_LOGON
 - ntsecapi/_KERB_TICKET_LOGON
 - PKERB_TICKET_LOGON
 - ntsecapi/PKERB_TICKET_LOGON
 - KERB_TICKET_LOGON
 - ntsecapi/KERB_TICKET_LOGON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_TICKET_LOGON
---

# KERB_TICKET_LOGON structure


## -description

The <b>KERB_TICKET_LOGON</b> structure contains profile information for a network logon.

It is used by the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function.

## -struct-fields

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_logon_submit_type">KERB_LOGON_SUBMIT_TYPE</a> value identifying the type of logon request being made. This member must be set to <b>KerbTicketLogon</b>.

### -field Flags

<b>ULONG</b> that can be set to KERB_LOGON_FLAG_ALLOW_EXPIRED_TICKET to allow a locked workstation to re-logon with expired ticket. Other values are ignored.

### -field ServiceTicketLength

Indicates the length of the <b>ServiceTicket</b> buffer.

### -field TicketGrantingTicketLength

Indicates the length of the <b>TicketGrantingTicket</b> buffer. Must be set to zero for an empty buffer.

### -field ServiceTicket

Required ticket for service "host" or the computer account <a href="/windows/desktop/SecGloss/s-gly">service principal name</a> (SPN) in the form of an <a href="/windows/desktop/SecGloss/a-gly">ASN.1</a> encoded Kerberos ticket. Expired tickets are acceptable if the <b>Flags</b> member is set to KERB_LOGON_FLAG_ALLOW_EXPIRED_TICKET.

### -field TicketGrantingTicket

Optional buffer containing an ASN.1-encoded KRB_CRED message containing the user's Kerberos ticket-granting ticket (KRBTGT) to be used to initialize the credential cache. The ticket must have the "forwarded" flag set in the ticket options. The KRB_CRED message is defined in Section 5.8 of  Internet <a href="http://www.ietf.org/rfc/rfc4120.txt">RFC 4120</a>. For more information, see <a href="https://www.ietf.org/">http://www.ietf.org</a>.

## -remarks

The service ticket must be for the host SPN of the computer. If the ticket includes a Windows Privilege Attribute Certificate (PAC), it will be used to construct the user's logon token. Otherwise, an anonymous token will be created using the client principal name in the ticket.

If a ticket-granting ticket (TGT) is supplied as a KRB_CRED message, it is placed in the <a href="/windows/desktop/SecGloss/l-gly">logon session</a> credentials cache. If the TGT is omitted, the logon will be only for the local machine.