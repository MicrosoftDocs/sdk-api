---
UID: NS:windnsdef.DNS_KEY_DATA
title: DNS_KEY_DATA (windnsdef.h)
description: The DNS_KEY_DATA structure represents a DNS key (KEY) resource record (RR) as specified in RFC 3445.
helpviewer_keywords: ["*PDNS_DNSKEY_DATA","*PDNS_KEY_DATA","1","2","3","4","5","DNS_DNSKEY_DATA","DNS_DNSKEY_DATA structure [DNS]","DNS_KEY_DATA","DNS_KEY_DATA structure [DNS]","PDNS_DNSKEY_DATA","PDNS_DNSKEY_DATA structure pointer [DNS]","PDNS_KEY_DATA","PDNS_KEY_DATA structure pointer [DNS]","_dns_dns_key_data","dns.dns_key_data","windnsdef/DNS_DNSKEY_DATA","windnsdef/DNS_KEY_DATA","windnsdef/PDNS_DNSKEY_DATA","windnsdef/PDNS_KEY_DATA"]
old-location: dns\dns_key_data.htm
tech.root: DNS
ms.assetid: d7d60322-4d06-4c57-b181-c6a38e09e1ef
ms.date: 01/15/2025
ms.keywords: '*PDNS_DNSKEY_DATA, *PDNS_KEY_DATA, 1, 2, 3, 4, 5, DNS_DNSKEY_DATA, DNS_DNSKEY_DATA structure [DNS], DNS_KEY_DATA, DNS_KEY_DATA structure [DNS], PDNS_DNSKEY_DATA, PDNS_DNSKEY_DATA structure pointer [DNS], PDNS_KEY_DATA, PDNS_KEY_DATA structure pointer [DNS], _dns_dns_key_data, dns.dns_key_data, windnsdef/DNS_DNSKEY_DATA, windnsdef/DNS_KEY_DATA, windnsdef/PDNS_DNSKEY_DATA, windnsdef/PDNS_KEY_DATA'
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
req.typenames: DNS_KEY_DATA, *PDNS_KEY_DATA, DNS_DNSKEY_DATA, *PDNS_DNSKEY_DATA
req.redist: 

f1_keywords:
 - PDNS_KEY_DATA
 - windnsdef/PDNS_KEY_DATA
 - DNS_KEY_DATA
 - windnsdef/DNS_KEY_DATA
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
 - DNS_KEY_DATA
---

# DNS_KEY_DATA structure


## -description

The 
<b>DNS_KEY_DATA</b> structure represents a DNS key (KEY) resource record (RR) as specified in <a href="https://www.ietf.org/rfc/rfc3445.txt">RFC 3445</a>.

## -struct-fields

### -field wFlags

A set of flags that specify whether this is a zone key as  described in section 4 of <a href="https://www.ietf.org/rfc/rfc3445.txt">RFC 3445</a>.

### -field chProtocol

A value that specifies the protocol with which <b>Key</b> can be used. The possible values are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Domain Name System Security Extensions (DNSSEC)

</td>
</tr>
</table>

### -field chAlgorithm

A value that specifies the algorithm to use with <b>Key</b>. The possible values are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
RSA/MD5 (<a href="https://www.ietf.org/rfc/rfc2537.txt">RFC 2537</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Diffie-Hellman (<a href="https://www.ietf.org/rfc/rfc2539.txt">RFC 2539</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
DSA (<a href="https://www.ietf.org/rfc/rfc2536.txt">RFC 2536</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
Elliptic curve cryptography

</td>
</tr>
<tr>
<td width="40%"><a id="5"></a><dl>
<dt><b>5</b></dt>
</dl>
</td>
<td width="60%">
RSA/SHA-1 (<a href="https://www.ietf.org/rfc/rfc3110.txt">RFC 3110</a>). <a href="/previous-versions/windows/desktop/legacy/dd392295(v=vs.85)">DNS_DNSKEY_DATA</a> only.

</td>
</tr>
</table>

### -field wKeyLength

The length, in bytes, of <b>Key</b>. This value is determined by the algorithm type in <b>chAlgorithm</b>.

### -field wPad

Reserved. Do not use.

### -field size_is

### -field size_is.wKeyLength

### -field Key

A <b>BYTE</b> array that contains the public key for the algorithm in <b>chAlgorithm</b>, represented in base 64, as described in Appendix A of <a href="https://www.ietf.org/rfc/rfc2535.txt">RFC 2535</a>.

## -remarks

The 
<b>DNS_KEY_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.

The <a href="/previous-versions/windows/desktop/legacy/dd392295(v=vs.85)">DNS_DNSKEY_DATA</a> structure represents a DNSKEY  resource record as specified in section 2 of  <a href="https://www.ietf.org/rfc/rfc4034.txt">RFC 4034</a>.

The 
<a href="/previous-versions/windows/desktop/legacy/dd392295(v=vs.85)">DNS_DNSKEY_DATA</a> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.

The value of the <b>wFlags</b> member for <a href="/previous-versions/windows/desktop/legacy/dd392295(v=vs.85)">DNS_DNSKEY_DATA</a> is a set of flags that specify key properties as  described in section 2.1.1 of <a href="https://www.ietf.org/rfc/rfc4034.txt">RFC 4034</a>.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

