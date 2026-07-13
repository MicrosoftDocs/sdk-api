---
UID: NS:windnsdef._DNS_HEADER
title: DNS_HEADER (windnsdef.h)
description: The DNS_HEADER structure contains DNS header information used when sending DNS messages as specified in section 4.1.1 of RFC 1035.
helpviewer_keywords: ["*PDNS_HEADER","*PDNS_HEADER structure [DNS]","DNS_HEADER","DNS_HEADER structure [DNS]","dns.dns_header","windnsdef/*PDNS_HEADER","windnsdef/DNS_HEADER"]
old-location: dns\dns_header.htm
tech.root: DNS
ms.assetid: e5bf19a1-4c71-482d-a075-1e149f94505b
ms.date: 01/15/2025
ms.keywords: '*PDNS_HEADER, *PDNS_HEADER structure [DNS], DNS_HEADER, DNS_HEADER structure [DNS], dns.dns_header, windnsdef/*PDNS_HEADER, windnsdef/DNS_HEADER'
req.header: windnsdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DNS_HEADER, *PDNS_HEADER
req.redist: 

f1_keywords:
 - _DNS_HEADER
 - windnsdef/_DNS_HEADER
 - PDNS_HEADER
 - windnsdef/PDNS_HEADER
 - DNS_HEADER
 - windnsdef/DNS_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windnsdef.h
api_name:
 - DNS_HEADER
---

# DNS_HEADER structure


## -description

The <b>DNS_HEADER</b> structure contains DNS header information used when sending DNS messages as specified in section 4.1.1 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>.

## -struct-fields

### -field Xid

A value that specifies the unique DNS message identifier.

### -field RecursionDesired

A value that specifies whether recursive name query should be used  by the DNS name server.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Do not use recursive name query.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Use recursive name query.

</td>
</tr>
</table>

### -field Truncation

A value that specifies whether the DNS message has been truncated.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
The message is not truncated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The message is truncated.

</td>
</tr>
</table>

### -field Authoritative

A value that  specifies whether the DNS server from which the DNS message is being sent is authoritative for the domain name's zone.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
The DNS server is not authoritative in the zone.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The DNS server is authoritative in the zone.

</td>
</tr>
</table>

### -field Opcode

A value that specifies the operation code to be taken on the DNS message as defined in section 4.1.1 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a> as the <b>OPCODE</b> field.

### -field IsResponse

A value that specifies whether the DNS message is a query or a response message.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
The DNS message is a query.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The DNS message is a response.

</td>
</tr>
</table>

### -field ResponseCode

The <a href="/windows/win32/DNS/dns-constants">DNS Response Code</a> of the message.

### -field CheckingDisabled

Windows 7 or later: A value that specifies whether checking is supported by the DNS resolver.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Checking is enabled on the DNS resolver.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Checking is disabled on the DNS resolver.

</td>
</tr>
</table>

### -field AuthenticatedData

Windows 7 or later: A value that specifies whether the DNS data following the <b>DNS_HEADER</b> is authenticated by the DNS server.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
The DNS data is not authenticated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The DNS data is authenticated.

</td>
</tr>
</table>

### -field Reserved

Reserved. Do not use.

### -field RecursionAvailable

A value that specifies whether recursive name query is supported by the DNS name server.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Recursive name query is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Recursive name query is supported.

</td>
</tr>
</table>

### -field QuestionCount

The number of queries contained in the question section of the DNS message.

### -field AnswerCount

The number of resource records (RRs) contained in the answer section of the DNS message.

### -field NameServerCount

The number of DNS name server RRs contained in the authority section of the DNS message. This value is the number of DNS name servers the message has traversed in its search for resolution.

### -field AdditionalCount

Reserved. Do not use.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>