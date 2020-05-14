---
UID: NS:windns.__unnamed_struct_17
title: DNS_SIG_DATAA (windns.h)
description: Structure represents a DNS Security Extensions (DNSSEC) cryptographic signature (SIG) resource record (RR) as specified in RFC 4034.
helpviewer_keywords: ["*PDNS_RRSIG_DATA","*PDNS_RRSIG_DATAA","*PDNS_SIG_DATA","*PDNS_SIG_DATAA","1","2","3","4","5","DNS_RRSIG_DATA","DNS_RRSIG_DATA structure [DNS]","DNS_RRSIG_DATAA","DNS_SIG_DATA","DNS_SIG_DATAA","PDNS_RRSIG_DATA","PDNS_RRSIG_DATA structure pointer [DNS]","dns.dns_rrsig_data","windns/DNS_RRSIG_DATA","windns/PDNS_RRSIG_DATA"]
old-location: dns\dns_rrsig_data.htm
tech.root: DNS
ms.assetid: 09c2f515-acc1-402f-8e62-a0d273031633
ms.date: 12/05/2018
ms.keywords: '*PDNS_RRSIG_DATA, *PDNS_RRSIG_DATAA, *PDNS_SIG_DATA, *PDNS_SIG_DATAA, 1, 2, 3, 4, 5, DNS_RRSIG_DATA, DNS_RRSIG_DATA structure [DNS], DNS_RRSIG_DATAA, DNS_SIG_DATA, DNS_SIG_DATAA, PDNS_RRSIG_DATA, PDNS_RRSIG_DATA structure pointer [DNS], dns.dns_rrsig_data, windns/DNS_RRSIG_DATA, windns/PDNS_RRSIG_DATA'
f1_keywords:
- windns/DNS_RRSIG_DATA
dev_langs:
- c++
req.header: windns.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Windns.h
api_name:
- DNS_RRSIG_DATA
targetos: Windows
req.typenames: DNS_SIG_DATAA, *PDNS_SIG_DATAA, DNS_RRSIG_DATAA, *PDNS_RRSIG_DATAA
req.redist: 
ms.custom: 19H1
---

# DNS_SIG_DATAA structure


## -description


The <b>DNS_RRSIG_DATA</b> structure represents a DNS
   Security Extensions (DNSSEC) cryptographic signature (SIG) resource  record (RR) as specified in <a href="https://www.ietf.org/rfc/rfc4034.txt">RFC 4034</a>.


## -struct-fields




### -field wTypeCovered

The <a href="https://docs.microsoft.com/windows/desktop/DNS/dns-constants">DNS Record Type</a> of the signed RRs.


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
<a href="/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DNS/dns-structures">DNS Structures</a>



<a href="/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>
 

 

