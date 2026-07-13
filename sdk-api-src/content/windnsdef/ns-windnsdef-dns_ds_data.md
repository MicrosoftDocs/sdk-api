---
UID: NS:windnsdef.DNS_DS_DATA
title: DNS_DS_DATA (windnsdef.h)
description: Represents a DS resource record (RR) as specified in section 2 of RFC 4034 and is used to verify the contents of DNS_DNSKEY_DATA.
helpviewer_keywords: ["*PDNS_DS_DATA","1","2","3","4","5","DNS_DS_DATA","DNS_DS_DATA structure [DNS]","PDNS_DS_DATA","PDNS_DS_DATA structure pointer [DNS]","dns.dns_ds_data","windnsdef/DNS_DS_DATA","windnsdef/PDNS_DS_DATA"]
old-location: dns\dns_ds_data.htm
tech.root: DNS
ms.assetid: 8624cc27-feb5-4e4a-8970-40aa1d43960e
ms.date: 01/15/2025
ms.keywords: '*PDNS_DS_DATA, 1, 2, 3, 4, 5, DNS_DS_DATA, DNS_DS_DATA structure [DNS], PDNS_DS_DATA, PDNS_DS_DATA structure pointer [DNS], dns.dns_ds_data, windnsdef/DNS_DS_DATA, windnsdef/PDNS_DS_DATA'
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
req.typenames: DNS_DS_DATA, *PDNS_DS_DATA
req.redist: 

f1_keywords:
 - PDNS_DS_DATA
 - windnsdef/PDNS_DS_DATA
 - DNS_DS_DATA
 - windnsdef/DNS_DS_DATA
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
 - DNS_DS_DATA
---

# DNS_DS_DATA structure


## -description

The <b>DNS_DS_DATA</b> structure represents a DS  resource record (RR) as specified in section 2 of  <a href="https://www.ietf.org/rfc/rfc4034.txt">RFC 4034</a> and is used to verify the contents of <a href="/previous-versions/windows/desktop/legacy/dd392295(v=vs.85)">DNS_DNSKEY_DATA</a>.

## -struct-fields

### -field wKeyTag

A value that represents the method to choose which public key is used to verify  <b>Signature</b> in <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_sig_dataw">DNS_RRSIG_DATA</a> as specified in Appendix B of <a href="https://www.ietf.org/rfc/rfc4034.txt">RFC 4034</a>. This value is identical to the <b>wKeyTag</b> field in <b>DNS_RRSIG_DATA</b>.

### -field chAlgorithm

A value that specifies the  algorithm defined by <a href="/previous-versions/windows/desktop/legacy/dd392295(v=vs.85)">DNS_DNSKEY_DATA</a>. The possible values are shown in the following table.

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

### -field chDigestType

A value that specifies the cryptographic algorithm used to generate <b>Digest</b>. The possible values are shown in the following table.

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
SHA-1 (<a href="https://www.ietf.org/rfc/rfc3174.txt">RFC 3174</a>)

</td>
</tr>
</table>

### -field wDigestLength

The length, in bytes. of the message digest in <b>Digest</b>. This value is determined by the algorithm type in <b>chDigestType</b>.

### -field wPad

Reserved for padding. Do not use.

### -field size_is

### -field size_is.wDigestLength

### -field Digest

A <b>BYTE</b> array that contains a cryptographic digest of the DNSKEY RR and RDATA as specified in section 5.1.4 of <a href="https://www.ietf.org/rfc/rfc4034.txt">RFC 4034</a>. Its length is determined by <b>wDigestLength</b>.

## -remarks

The 
<b>DNS_DS_DATA</b> structure is used in conjunction with the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.

## -see-also

<a href="/windows/win32/DNS/dns-structures">DNS Structures</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>

