---
UID: NS:windns.__unnamed_struct_25
title: DNS_DS_DATA
author: windows-sdk-content
description: Represents a DS resource record (RR) as specified in section 2 of RFC 4034 and is used to verify the contents of DNS_DNSKEY_DATA.
old-location: dns\dns_ds_data.htm
old-project: dns
ms.assetid: 8624cc27-feb5-4e4a-8970-40aa1d43960e
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PDNS_DS_DATA, 1, 2, 3, 4, 5, DNS_DS_DATA, DNS_DS_DATA structure [DNS], PDNS_DS_DATA, PDNS_DS_DATA structure pointer [DNS], dns.dns_ds_data, windns/DNS_DS_DATA, windns/PDNS_DS_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DNS_DS_DATA, *PDNS_DS_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_DS_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DNS_DS_DATA structure


## -description


The <b>DNS_DS_DATA</b> structure represents a DS  resource record (RR) as specified in section 2 of  <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a> and is used to verify the contents of <a href="https://msdn.microsoft.com/5c15980f-6dc7-4b6d-8be1-e22fdea8fe67">DNS_DNSKEY_DATA</a>.


## -struct-fields




### -field wKeyTag

A value that represents the method to choose which public key is used to verify  <b>Signature</b> in <a href="https://msdn.microsoft.com/09c2f515-acc1-402f-8e62-a0d273031633">DNS_RRSIG_DATA</a> as specified in Appendix B of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>. This value is identical to the <b>wKeyTag</b> field in <b>DNS_RRSIG_DATA</b>.


### -field chAlgorithm

A value that specifies the  algorithm defined by <a href="https://msdn.microsoft.com/5c15980f-6dc7-4b6d-8be1-e22fdea8fe67">DNS_DNSKEY_DATA</a>. The possible values are shown in the following table.

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
RSA/MD5 (<a href="http://go.microsoft.com/fwlink/p/?linkid=124777">RFC 2537</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Diffie-Hellman (<a href=" http://go.microsoft.com/fwlink/p/?linkid=124778">RFC 2539</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
DSA (<a href="http://go.microsoft.com/fwlink/p/?linkid=124779">RFC 2536</a>)

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
RSA/SHA-1 (<a href="http://go.microsoft.com/fwlink/p/?linkid=90406">RFC 3110</a>)

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
SHA-1 (<a href="http://go.microsoft.com/fwlink/p/?linkid=90408">RFC 3174</a>)

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

A <b>BYTE</b> array that contains a cryptographic digest of the DNSKEY RR and RDATA as specified in section 5.1.4 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>. Its length is determined by <b>wDigestLength</b>.


## -remarks



The 
<b>DNS_DS_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/636399be-43a5-4ddf-b652-f8efb81fbf42">DNS Structures</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

