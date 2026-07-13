---
UID: NS:windnsdef.DNS_SIG_DATAW
title: DNS_SIG_DATAW (windnsdef.h)
description: Structure represents a DNS Security Extensions (DNSSEC) cryptographic signature (SIG) resource record (RR) as specified in RFC 4034. (Unicode)
helpviewer_keywords: ["*PDNS_RRSIG_DATA","*PDNS_RRSIG_DATAW","*PDNS_SIG_DATA","*PDNS_SIG_DATAW","1","2","3","4","5","DNS_RRSIG_DATA","DNS_RRSIG_DATA structure [DNS]","DNS_RRSIG_DATAW","DNS_SIG_DATA","DNS_SIG_DATAW","PDNS_RRSIG_DATA","PDNS_RRSIG_DATA structure pointer [DNS]","dns.dns_rrsig_data","windnsdef/DNS_RRSIG_DATA","windnsdef/PDNS_RRSIG_DATA"]
old-location: dns\dns_rrsig_data.htm
tech.root: DNS
ms.assetid: 09c2f515-acc1-402f-8e62-a0d273031633
ms.date: 01/15/2025
ms.keywords: '*PDNS_RRSIG_DATA, *PDNS_RRSIG_DATAW, *PDNS_SIG_DATA, *PDNS_SIG_DATAW, 1, 2, 3, 4, 5, DNS_RRSIG_DATA, DNS_RRSIG_DATA structure [DNS], DNS_RRSIG_DATAW, DNS_SIG_DATA, DNS_SIG_DATAW, PDNS_RRSIG_DATA, PDNS_RRSIG_DATA structure pointer [DNS], dns.dns_rrsig_data, windnsdef/DNS_RRSIG_DATA, windnsdef/PDNS_RRSIG_DATA'
req.header: windnsdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DNS_SIG_DATAW, *PDNS_SIG_DATAW, DNS_RRSIG_DATAW, *PDNS_RRSIG_DATAW
req.redist: 

f1_keywords:
 - PDNS_SIG_DATAW
 - windnsdef/PDNS_SIG_DATAW
 - DNS_SIG_DATAW
 - windnsdef/DNS_SIG_DATAW
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
 - DNS_RRSIG_DATA
---

# DNS_SIG_DATAW structure


## -description

The <b>DNS_RRSIG_DATA</b> structure represents a DNS
   Security Extensions (DNSSEC) cryptographic signature (SIG) resource  record (RR) as specified in <a href="https://www.ietf.org/rfc/rfc4034.txt">RFC 4034</a>.

## -struct-fields

### -field wTypeCovered

The <a href="/windows/win32/DNS/dns-constants">DNS Record Type</a> of the signed RRs.

### -field chAlgorithm

A value that specifies the  algorithm used to generate <b>Signature</b>. The possible values are shown in the following table.

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
RSA/SHA-1 (<a href="https://www.ietf.org/rfc/rfc3110.txt">RFC 3110</a>)

</td>
</tr>
</table>

### -field chLabelCount

The number of labels in the original signature RR owner name as specified in section 3.1.3 of <a href="https://www.ietf.org/rfc/rfc4034.txt">RFC 4034</a>.

### -field dwOriginalTtl

The Time-to-Live (TTL) value of the RR set signed by <b>Signature</b>.

### -field dwExpiration

The expiration date of <b>Signature</b>, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.

### -field dwTimeSigned

The date and time at which <b>Signature</b> becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.

### -field wKeyTag

A value that represents the method to choose which public key is used to verify  <b>Signature</b> as specified Appendix B of <a href="https://www.ietf.org/rfc/rfc4034.txt">RFC 4034</a>.

### -field wSignatureLength

### -field pNameSigner

A pointer to a string that represents  the name of the <b>Signature</b> generator.

### -field size_is

### -field size_is.wSignatureLength

### -field Signature

A <b>BYTE</b> array that contains the RR set signature as specified in section 3.1.8 of <a href="https://www.ietf.org/rfc/rfc4034.txt">RFC 4034</a>.


#### - Pad

Reserved for padding. Do not use.

## -remarks

The 
<b>DNS_RRSIG_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.





> [!NOTE]
> The windns.h header defines DNS_SIG_DATA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/DNS/dns-structures">DNS Structures</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

