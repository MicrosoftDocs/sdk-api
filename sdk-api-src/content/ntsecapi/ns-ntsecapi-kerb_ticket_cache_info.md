---
UID: NS:ntsecapi._KERB_TICKET_CACHE_INFO
title: KERB_TICKET_CACHE_INFO (ntsecapi.h)
description: Contains information about a cached Kerberos ticket. The Kerberos ticket is defined in Internet RFC 4120. For more information, see http://www.ietf.org.
helpviewer_keywords: ["*PKERB_TICKET_CACHE_INFO","KERB_TICKET_CACHE_INFO","KERB_TICKET_CACHE_INFO structure [Security]","KERB_TICKET_FLAGS_forwardable","KERB_TICKET_FLAGS_forwarded","KERB_TICKET_FLAGS_hw_authent","KERB_TICKET_FLAGS_initial","KERB_TICKET_FLAGS_invalid","KERB_TICKET_FLAGS_may_postdate","KERB_TICKET_FLAGS_ok_as_delegate","KERB_TICKET_FLAGS_postdated","KERB_TICKET_FLAGS_pre_authent","KERB_TICKET_FLAGS_proxiable","KERB_TICKET_FLAGS_proxy","KERB_TICKET_FLAGS_renewable","KERB_TICKET_FLAGS_reserved","KERB_TICKET_FLAGS_reserved1","PKERB_TICKET_CACHE_INFO","PKERB_TICKET_CACHE_INFO structure pointer [Security]","_lsa_kerb_ticket_cache_info","ntsecapi/KERB_TICKET_CACHE_INFO","ntsecapi/PKERB_TICKET_CACHE_INFO","security.kerb_ticket_cache_info"]
old-location: security\kerb_ticket_cache_info.htm
tech.root: security
ms.assetid: e9ac70f0-65dc-4c5a-b41f-7c4659680333
ms.date: 12/05/2018
ms.keywords: '*PKERB_TICKET_CACHE_INFO, KERB_TICKET_CACHE_INFO, KERB_TICKET_CACHE_INFO structure [Security], KERB_TICKET_FLAGS_forwardable, KERB_TICKET_FLAGS_forwarded, KERB_TICKET_FLAGS_hw_authent, KERB_TICKET_FLAGS_initial, KERB_TICKET_FLAGS_invalid, KERB_TICKET_FLAGS_may_postdate, KERB_TICKET_FLAGS_ok_as_delegate, KERB_TICKET_FLAGS_postdated, KERB_TICKET_FLAGS_pre_authent, KERB_TICKET_FLAGS_proxiable, KERB_TICKET_FLAGS_proxy, KERB_TICKET_FLAGS_renewable, KERB_TICKET_FLAGS_reserved, KERB_TICKET_FLAGS_reserved1, PKERB_TICKET_CACHE_INFO, PKERB_TICKET_CACHE_INFO structure pointer [Security], _lsa_kerb_ticket_cache_info, ntsecapi/KERB_TICKET_CACHE_INFO, ntsecapi/PKERB_TICKET_CACHE_INFO, security.kerb_ticket_cache_info'
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
req.typenames: KERB_TICKET_CACHE_INFO, *PKERB_TICKET_CACHE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _KERB_TICKET_CACHE_INFO
 - ntsecapi/_KERB_TICKET_CACHE_INFO
 - PKERB_TICKET_CACHE_INFO
 - ntsecapi/PKERB_TICKET_CACHE_INFO
 - KERB_TICKET_CACHE_INFO
 - ntsecapi/KERB_TICKET_CACHE_INFO
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
 - KERB_TICKET_CACHE_INFO
---

# KERB_TICKET_CACHE_INFO structure


## -description

The <b>KERB_TICKET_CACHE_INFO</b> structure contains information about a cached <a href="/windows/desktop/SecGloss/k-gly">Kerberos</a> ticket. The Kerberos ticket is defined in Internet <a href="http://www.ietf.org/rfc/rfc4120.txt">RFC 4120</a>. For more information, see <a href="https://www.ietf.org/">http://www.ietf.org</a>.

It can be used both for retrieving tickets and querying the ticket cache. The 
<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-kerb_query_tkt_cache_response">KERB_QUERY_TKT_CACHE_RESPONSE</a> structure uses this structure.

## -struct-fields

### -field ServerName

A
						<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that contains the name of the server the ticket applies to. This name is combined with the <b>RealmName</b> value to create the full name <b>ServerName</b>@<b>RealmName</b>.

### -field RealmName

A <a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that contains the name of the realm the ticket applies to.

### -field StartTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time at which the ticket becomes valid. If the <b>starttime</b> member of the ticket is not set, this value defaults to the time when the ticket was initially authenticated, <b>authtime</b>. The <b>starttime</b> member of a ticket is optional.

### -field EndTime

A <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time when the ticket expires.

### -field RenewTime

If KERB_TICKET_FLAGS_renewable is set in <b>TicketFlags</b>, this member is a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time beyond which the ticket cannot be renewed.

### -field EncryptionType

The type of encryption used in the ticket.

### -field TicketFlags

The ticket flags, as defined in Internet <a href="http://www.ietf.org/rfc/rfc4120.txt">RFC 4120</a>. These flags can be one or more of the following values. 





<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_forwardable"></a><a id="kerb_ticket_flags_forwardable"></a><a id="KERB_TICKET_FLAGS_FORWARDABLE"></a><dl>
<dt><b>KERB_TICKET_FLAGS_forwardable</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
The ticket-granting server can issue a new ticket-granting ticket with a different network address based on the presented ticket.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_forwarded"></a><a id="kerb_ticket_flags_forwarded"></a><a id="KERB_TICKET_FLAGS_FORWARDED"></a><dl>
<dt><b>KERB_TICKET_FLAGS_forwarded</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
The ticket has either been forwarded or was issued based on authentication that involved a forwarded ticket-granting ticket.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_hw_authent"></a><a id="kerb_ticket_flags_hw_authent"></a><a id="KERB_TICKET_FLAGS_HW_AUTHENT"></a><dl>
<dt><b>KERB_TICKET_FLAGS_hw_authent</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
The protocol employed for initial authentication required the use of hardware expected to be possessed solely by the named client. The hardware authentication method is selected by the KDC and the strength of the method is not indicated.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_initial"></a><a id="kerb_ticket_flags_initial"></a><a id="KERB_TICKET_FLAGS_INITIAL"></a><dl>
<dt><b>KERB_TICKET_FLAGS_initial</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
The ticket was issued by using the Authentication Service protocol instead of being based on a ticket-granting ticket.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_invalid"></a><a id="kerb_ticket_flags_invalid"></a><a id="KERB_TICKET_FLAGS_INVALID"></a><dl>
<dt><b>KERB_TICKET_FLAGS_invalid</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
The ticket is not valid.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_may_postdate"></a><a id="kerb_ticket_flags_may_postdate"></a><a id="KERB_TICKET_FLAGS_MAY_POSTDATE"></a><dl>
<dt><b>KERB_TICKET_FLAGS_may_postdate</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
Indicates to the ticket-granting server that a postdated ticket can be issued based on this ticket-granting ticket.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_ok_as_delegate"></a><a id="kerb_ticket_flags_ok_as_delegate"></a><a id="KERB_TICKET_FLAGS_OK_AS_DELEGATE"></a><dl>
<dt><b>KERB_TICKET_FLAGS_ok_as_delegate</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The target of the ticket is trusted by the directory service for delegation. Thus, clients may delegate their <a href="/windows/desktop/SecGloss/c-gly">credentials</a> to the server, which lets the server act as the client when talking to other services.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_postdated"></a><a id="kerb_ticket_flags_postdated"></a><a id="KERB_TICKET_FLAGS_POSTDATED"></a><dl>
<dt><b>KERB_TICKET_FLAGS_postdated</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
The ticket has been postdated. The end-service can check the ticket's <b>authtime</b> member to see when the original authentication occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_pre_authent"></a><a id="kerb_ticket_flags_pre_authent"></a><a id="KERB_TICKET_FLAGS_PRE_AUTHENT"></a><dl>
<dt><b>KERB_TICKET_FLAGS_pre_authent</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
During initial authentication, the client was authenticated by the <a href="/windows/desktop/SecGloss/k-gly">Key Distribution Center</a> (KDC) before a ticket was issued. The strength of the preauthentication method is not indicated, but is acceptable to the KDC.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_proxiable"></a><a id="kerb_ticket_flags_proxiable"></a><a id="KERB_TICKET_FLAGS_PROXIABLE"></a><dl>
<dt><b>KERB_TICKET_FLAGS_proxiable</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Indicates to the ticket-granting server that only nonticket-granting tickets can be issued based on this ticket but with a different network addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_proxy"></a><a id="kerb_ticket_flags_proxy"></a><a id="KERB_TICKET_FLAGS_PROXY"></a><dl>
<dt><b>KERB_TICKET_FLAGS_proxy</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
The ticket is a proxy.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_renewable"></a><a id="kerb_ticket_flags_renewable"></a><a id="KERB_TICKET_FLAGS_RENEWABLE"></a><dl>
<dt><b>KERB_TICKET_FLAGS_renewable</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
The ticket is renewable. If this flag is set, the time limit for renewing the ticket is set in <b>RenewTime</b>. A renewable ticket can be used to obtain a replacement ticket that expires at a later date.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_reserved"></a><a id="kerb_ticket_flags_reserved"></a><a id="KERB_TICKET_FLAGS_RESERVED"></a><dl>
<dt><b>KERB_TICKET_FLAGS_reserved</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Reserved for future use. Do not set this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="KERB_TICKET_FLAGS_reserved1"></a><a id="kerb_ticket_flags_reserved1"></a><a id="KERB_TICKET_FLAGS_RESERVED1"></a><dl>
<dt><b>KERB_TICKET_FLAGS_reserved1</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
</table>