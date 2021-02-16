---
UID: NS:ntsecapi._KERB_EXTERNAL_TICKET
title: KERB_EXTERNAL_TICKET (ntsecapi.h)
description: Contains information about an external ticket.
helpviewer_keywords: ["*PKERB_EXTERNAL_TICKET","KERB_EXTERNAL_TICKET","KERB_EXTERNAL_TICKET structure [Security]","KERB_TICKET_FLAGS_forwardable (0x40000000)","KERB_TICKET_FLAGS_forwarded (0x20000000)","KERB_TICKET_FLAGS_hw_authent (0x00100000)","KERB_TICKET_FLAGS_initial (0x00400000)","KERB_TICKET_FLAGS_invalid (0x01000000)","KERB_TICKET_FLAGS_may_postdate (0x04000000)","KERB_TICKET_FLAGS_ok_as_delegate (0x00040000)","KERB_TICKET_FLAGS_postdated (0x02000000)","KERB_TICKET_FLAGS_pre_authent (0x00200000)","KERB_TICKET_FLAGS_proxiable (0x10000000)","KERB_TICKET_FLAGS_proxy (0x08000000)","KERB_TICKET_FLAGS_renewable (0x00800000)","KERB_TICKET_FLAGS_reserved (0x80000000)","KERB_TICKET_FLAGS_reserved1 (0x00000001)","PKERB_EXTERNAL_TICKET","PKERB_EXTERNAL_TICKET structure pointer [Security]","_lsa_kerb_external_ticket","ntsecapi/KERB_EXTERNAL_TICKET","ntsecapi/PKERB_EXTERNAL_TICKET","security.kerb_external_ticket"]
old-location: security\kerb_external_ticket.htm
tech.root: security
ms.assetid: 742e2795-ec74-4856-a680-7a1c233a2934
ms.date: 12/05/2018
ms.keywords: '*PKERB_EXTERNAL_TICKET, KERB_EXTERNAL_TICKET, KERB_EXTERNAL_TICKET structure [Security], KERB_TICKET_FLAGS_forwardable (0x40000000), KERB_TICKET_FLAGS_forwarded (0x20000000), KERB_TICKET_FLAGS_hw_authent (0x00100000), KERB_TICKET_FLAGS_initial (0x00400000), KERB_TICKET_FLAGS_invalid (0x01000000), KERB_TICKET_FLAGS_may_postdate (0x04000000), KERB_TICKET_FLAGS_ok_as_delegate (0x00040000), KERB_TICKET_FLAGS_postdated (0x02000000), KERB_TICKET_FLAGS_pre_authent (0x00200000), KERB_TICKET_FLAGS_proxiable (0x10000000), KERB_TICKET_FLAGS_proxy (0x08000000), KERB_TICKET_FLAGS_renewable (0x00800000), KERB_TICKET_FLAGS_reserved (0x80000000), KERB_TICKET_FLAGS_reserved1 (0x00000001), PKERB_EXTERNAL_TICKET, PKERB_EXTERNAL_TICKET structure pointer [Security], _lsa_kerb_external_ticket, ntsecapi/KERB_EXTERNAL_TICKET, ntsecapi/PKERB_EXTERNAL_TICKET, security.kerb_external_ticket'
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
req.typenames: KERB_EXTERNAL_TICKET, *PKERB_EXTERNAL_TICKET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_EXTERNAL_TICKET
 - ntsecapi/_KERB_EXTERNAL_TICKET
 - PKERB_EXTERNAL_TICKET
 - ntsecapi/PKERB_EXTERNAL_TICKET
 - KERB_EXTERNAL_TICKET
 - ntsecapi/KERB_EXTERNAL_TICKET
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
 - KERB_EXTERNAL_TICKET
---

# KERB_EXTERNAL_TICKET structure


## -description

The <b>KERB_EXTERNAL_TICKET</b> structure contains information about an external ticket.

An external ticket is a <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> ticket exported to external users. The Kerberos ticket is defined in Internet <a href="http://www.ietf.org/rfc/rfc4120.txt">RFC 4120</a>. For more information, see <a href="https://www.ietf.org/">http://www.ietf.org</a>. This structure is used by the 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_retrieve_tkt_response">KERB_RETRIEVE_TKT_RESPONSE</a> structure.

## -struct-fields

### -field ServiceName

A <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_external_name">KERB_EXTERNAL_NAME</a> structure that contains a multiple part, canonical, returned service name.

### -field TargetName

A <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_external_name">KERB_EXTERNAL_NAME</a> structure that contains the multiple part <a href="/windows/desktop/SecGloss/s-gly">service principal name</a> (SPN).

### -field ClientName

A <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_external_name">KERB_EXTERNAL_NAME</a> structure that contains the client name in the ticket. This name is relative to the current domain.

### -field DomainName

A
						<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that contains the name of the domain that corresponds to the <b>ServiceName</b> member. This is the domain that issued the ticket.

### -field TargetDomainName

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that contains the name of the domain in which the ticket is valid. For an interdomain ticket, this is the destination domain.

### -field AltTargetDomainName

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that contains a synonym for the destination domain. Every domain has two names: a DNS name and a NetBIOS name. If the name returned in the ticket is different from the name used to request the ticket (the Kerberos <a href="/windows/desktop/SecGloss/k-gly">Key Distribution Center</a> (KDC) may do name mapping), this string contains the original name.

### -field SessionKey

A <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_crypto_key">KERB_CRYPTO_KEY</a> structure that contains the <a href="/windows/desktop/SecGloss/s-gly">session key</a> for the ticket.

### -field TicketFlags

Ticket flags, as defined in Internet <a href="http://www.ietf.org/rfc/rfc4120.txt">RFC 4120</a>. This parameter can be one or more of the following values. 





<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_forwardable__0x40000000_"></a><a id="kerb_ticket_flags_forwardable__0x40000000_"></a><a id="KERB_TICKET_FLAGS_FORWARDABLE__0X40000000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_forwardable
(0x40000000)</b></dt>
</dl>
</td>
<td width="60%">
The ticket-granting server can issue a new ticket-granting ticket with a different network address, based on the presented ticket.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_forwarded__0x20000000_"></a><a id="kerb_ticket_flags_forwarded__0x20000000_"></a><a id="KERB_TICKET_FLAGS_FORWARDED__0X20000000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_forwarded
(0x20000000)</b></dt>
</dl>
</td>
<td width="60%">
The ticket has either been forwarded or was issued based on authentication that involved a forwarded ticket-granting ticket.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_hw_authent__0x00100000_"></a><a id="kerb_ticket_flags_hw_authent__0x00100000_"></a><a id="KERB_TICKET_FLAGS_HW_AUTHENT__0X00100000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_hw_authent
(0x00100000)</b></dt>
</dl>
</td>
<td width="60%">
The protocol employed for initial authentication required the use of hardware expected to be possessed solely by the named client. The hardware authentication method is selected by the KDC, and the strength of the method is not indicated.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_initial__0x00400000_"></a><a id="kerb_ticket_flags_initial__0x00400000_"></a><a id="KERB_TICKET_FLAGS_INITIAL__0X00400000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_initial
(0x00400000)</b></dt>
</dl>
</td>
<td width="60%">
The ticket was issued by using the Authentication Service protocol instead of being based on a ticket-granting ticket.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_invalid__0x01000000_"></a><a id="kerb_ticket_flags_invalid__0x01000000_"></a><a id="KERB_TICKET_FLAGS_INVALID__0X01000000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_invalid
(0x01000000)</b></dt>
</dl>
</td>
<td width="60%">
The ticket is not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_may_postdate__0x04000000_"></a><a id="kerb_ticket_flags_may_postdate__0x04000000_"></a><a id="KERB_TICKET_FLAGS_MAY_POSTDATE__0X04000000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_may_postdate
(0x04000000)</b></dt>
</dl>
</td>
<td width="60%">
Indicates to the ticket-granting server that a postdated ticket can be issued based on this ticket-granting ticket.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_ok_as_delegate__0x00040000_"></a><a id="kerb_ticket_flags_ok_as_delegate__0x00040000_"></a><a id="KERB_TICKET_FLAGS_OK_AS_DELEGATE__0X00040000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_ok_as_delegate
(0x00040000)</b></dt>
</dl>
</td>
<td width="60%">
The target of the ticket is trusted by the directory service for delegation. Thus, the clients may delegate their <a href="/windows/desktop/SecGloss/c-gly">credentials</a> to the server, which lets the server act as the client when talking to other services.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_postdated__0x02000000_"></a><a id="kerb_ticket_flags_postdated__0x02000000_"></a><a id="KERB_TICKET_FLAGS_POSTDATED__0X02000000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_postdated
(0x02000000)</b></dt>
</dl>
</td>
<td width="60%">
The ticket has been postdated. The end service can check the ticket's <b>authtime</b> member to determine when the original authentication occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_pre_authent__0x00200000_"></a><a id="kerb_ticket_flags_pre_authent__0x00200000_"></a><a id="KERB_TICKET_FLAGS_PRE_AUTHENT__0X00200000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_pre_authent
(0x00200000)</b></dt>
</dl>
</td>
<td width="60%">
During initial authentication, the client was authenticated by the KDC before a ticket was issued. The strength of the preauthentication method is not indicated but is acceptable to the KDC.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_proxiable__0x10000000_"></a><a id="kerb_ticket_flags_proxiable__0x10000000_"></a><a id="KERB_TICKET_FLAGS_PROXIABLE__0X10000000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_proxiable
(0x10000000)</b></dt>
</dl>
</td>
<td width="60%">
Indicates to the ticket-granting server that only nonticket-granting tickets can be issued with different network addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_proxy__0x08000000_"></a><a id="kerb_ticket_flags_proxy__0x08000000_"></a><a id="KERB_TICKET_FLAGS_PROXY__0X08000000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_proxy
(0x08000000)</b></dt>
</dl>
</td>
<td width="60%">
The ticket is a proxy.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_renewable__0x00800000_"></a><a id="kerb_ticket_flags_renewable__0x00800000_"></a><a id="KERB_TICKET_FLAGS_RENEWABLE__0X00800000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_renewable
(0x00800000)</b></dt>
</dl>
</td>
<td width="60%">
The ticket is renewable. If this flag is set, the time limit for renewing the ticket is set in the <b>RenewTime</b> member of a <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_ticket_cache_info">KERB_TICKET_CACHE_INFO</a> structure. A renewable ticket can be used to obtain a replacement ticket that expires at a later date.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_reserved__0x80000000_"></a><a id="kerb_ticket_flags_reserved__0x80000000_"></a><a id="KERB_TICKET_FLAGS_RESERVED__0X80000000_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_reserved
(0x80000000)</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use. Do not set this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_reserved1__0x00000001_"></a><a id="kerb_ticket_flags_reserved1__0x00000001_"></a><a id="KERB_TICKET_FLAGS_RESERVED1__0X00000001_"></a><dl>
<dt><b>KERB_TICKET_FLAGS_reserved1
(0x00000001)</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
</table>

### -field Flags

Reserved for future use. Set this member to zero.

### -field KeyExpirationTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time at which the key expires.

### -field StartTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time at which the ticket becomes valid.

### -field EndTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time at which the ticket expires.

### -field RenewUntil

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the latest time a ticket can be renewed. Renewal requests sent after this time will be rejected.

### -field TimeSkew

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the measured time difference between the current time on the computer issuing the ticket and the computer where the ticket will be used.

### -field EncodedTicketSize

The size, in bytes, of the encoded ticket.

### -field EncodedTicket

A buffer that contains the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded ticket.