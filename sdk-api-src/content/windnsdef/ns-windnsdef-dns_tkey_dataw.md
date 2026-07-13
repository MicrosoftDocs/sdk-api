---
UID: NS:windnsdef.DNS_TKEY_DATAW
title: DNS_TKEY_DATAW (windnsdef.h)
description: The DNS_TKEY_DATA structure represents a DNS TKEY resource record, used to establish and delete an algorithm's shared-secret keys between a DNS resolver and server as specified in RFC 2930. (Unicode)
helpviewer_keywords: ["*PDNS_TKEY_DATA","*PDNS_TKEY_DATAW","DNS_RCODE_BADKEY","DNS_RCODE_BADSIG","DNS_RCODE_BADTIME","DNS_TKEY_DATA","DNS_TKEY_DATA structure [DNS]","DNS_TKEY_DATAW","DNS_TKEY_MODE_DIFFIE_HELLMAN","DNS_TKEY_MODE_GSS","DNS_TKEY_MODE_RESOLVER_ASSIGN","DNS_TKEY_MODE_SERVER_ASSIGN","PDNS_TKEY_DATA","PDNS_TKEY_DATA structure pointer [DNS]","_dns_dns_tkey_data","dns.dns_tkey_data","windnsdef/DNS_TKEY_DATA","windnsdef/PDNS_TKEY_DATA"]
old-location: dns\dns_tkey_data.htm
tech.root: DNS
ms.assetid: 4dad3449-3e41-47d9-89c2-10fa6e51573b
ms.date: 01/15/2025
ms.keywords: '*PDNS_TKEY_DATA, *PDNS_TKEY_DATAW, DNS_RCODE_BADKEY, DNS_RCODE_BADSIG, DNS_RCODE_BADTIME, DNS_TKEY_DATA, DNS_TKEY_DATA structure [DNS], DNS_TKEY_DATAW, DNS_TKEY_MODE_DIFFIE_HELLMAN, DNS_TKEY_MODE_GSS, DNS_TKEY_MODE_RESOLVER_ASSIGN, DNS_TKEY_MODE_SERVER_ASSIGN, PDNS_TKEY_DATA, PDNS_TKEY_DATA structure pointer [DNS], _dns_dns_tkey_data, dns.dns_tkey_data, windnsdef/DNS_TKEY_DATA, windnsdef/PDNS_TKEY_DATA'
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
req.typenames: DNS_TKEY_DATAW, *PDNS_TKEY_DATAW
req.redist: 

f1_keywords:
 - PDNS_TKEY_DATAW
 - windnsdef/PDNS_TKEY_DATAW
 - DNS_TKEY_DATAW
 - windnsdef/DNS_TKEY_DATAW
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
 - DNS_TKEY_DATA
---

# DNS_TKEY_DATAW structure


## -description

The 
<b>DNS_TKEY_DATA</b> structure represents a DNS TKEY resource record, used to establish and delete an algorithm's shared-secret keys between a DNS resolver and server as specified in <a href="https://www.ietf.org/rfc/rfc2930.txt">RFC 2930</a>.

## -struct-fields

### -field pNameAlgorithm

A pointer to a string that represents the name of the key as defined in section 2.1 of <a href="https://www.ietf.org/rfc/rfc2930.txt">RFC 2930</a>.

### -field pAlgorithmPacket

A pointer to a string representing the name of the   algorithm as defined in section 2.3 of <a href="https://www.ietf.org/rfc/rfc2930.txt">RFC 2930</a>. <b>pKey</b> is used to derive the algorithm specific keys.

### -field pKey

A pointer to the variable-length shared-secret key.

### -field pOtherData

Reserved. Do not use.

### -field dwCreateTime

The date and time at which the key was created, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.

### -field dwExpireTime

The expiration date of the key, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.

### -field wMode

A scheme used for key agreement or the purpose of the TKEY DNS Message. Possible values for <b>wMode</b> are listed below:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DNS_TKEY_MODE_SERVER_ASSIGN"></a><a id="dns_tkey_mode_server_assign"></a><dl>
<dt><b>DNS_TKEY_MODE_SERVER_ASSIGN</b></dt>
</dl>
</td>
<td width="60%">
The key is assigned by the DNS server and is not negotiated.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_TKEY_MODE_DIFFIE_HELLMAN"></a><a id="dns_tkey_mode_diffie_hellman"></a><dl>
<dt><b>DNS_TKEY_MODE_DIFFIE_HELLMAN</b></dt>
</dl>
</td>
<td width="60%">
The Diffie-Hellman key exchange algorithm is used to negotiate the key.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_TKEY_MODE_GSS_"></a><a id="dns_tkey_mode_gss_"></a><dl>
<dt><b>DNS_TKEY_MODE_GSS </b></dt>
</dl>
</td>
<td width="60%">
The key is exchanged through Generic Security Services-Application Program Interface (GSS-API) negotiation.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_TKEY_MODE_RESOLVER_ASSIGN"></a><a id="dns_tkey_mode_resolver_assign"></a><dl>
<dt><b>DNS_TKEY_MODE_RESOLVER_ASSIGN</b></dt>
</dl>
</td>
<td width="60%">
The key is assigned by the DNS resolver and is not negotiated.

</td>
</tr>
</table>

### -field wError

An error, expressed in expanded RCODE format that covers TSIG and TKEY RR processing.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DNS_RCODE_BADSIG"></a><a id="dns_rcode_badsig"></a><dl>
<dt><b>DNS_RCODE_BADSIG</b></dt>
</dl>
</td>
<td width="60%">
The <b>pSignature</b> of the <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_tsig_dataw">DNS_TSIG_DATA</a> RR is bad.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_RCODE_BADKEY"></a><a id="dns_rcode_badkey"></a><dl>
<dt><b>DNS_RCODE_BADKEY</b></dt>
</dl>
</td>
<td width="60%">
The <b>pKey</b> field is bad.

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_RCODE_BADTIME"></a><a id="dns_rcode_badtime"></a><dl>
<dt><b>DNS_RCODE_BADTIME</b></dt>
</dl>
</td>
<td width="60%">
A timestamp is bad.

</td>
</tr>
</table>

### -field wKeyLength

Length, in bytes, of the <b>pKey</b> member.

### -field wOtherLength

The length, in bytes, of the <b>pOtherData</b> member.

### -field cAlgNameLength

The length, in bytes, of the <b>pNameAlgorithm</b> member.

### -field bPacketPointers

Reserved. Do not use.

## -remarks

The 
<b>DNS_TKEY_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.





> [!NOTE]
> The windns.h header defines DNS_TKEY_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_tsig_dataw">DNS_TSIG_DATA</a>

