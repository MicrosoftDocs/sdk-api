---
UID: NS:windns.__unnamed_struct_18
title: DNS_KEY_DATA
author: windows-sdk-content
description: The DNS_KEY_DATA structure represents a DNS key (KEY) resource record (RR) as specified in RFC 3445.
old-location: dns\dns_key_data.htm
old-project: DNS
ms.assetid: d7d60322-4d06-4c57-b181-c6a38e09e1ef
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: "*PDNS_DNSKEY_DATA, *PDNS_KEY_DATA, 1, 2, 3, 4, 5, DNS_DNSKEY_DATA, DNS_DNSKEY_DATA structure [DNS], DNS_KEY_DATA, DNS_KEY_DATA structure [DNS], PDNS_DNSKEY_DATA, PDNS_DNSKEY_DATA structure pointer [DNS], PDNS_KEY_DATA, PDNS_KEY_DATA structure pointer [DNS], _dns_dns_key_data, dns.dns_key_data, windns/DNS_DNSKEY_DATA, windns/DNS_KEY_DATA, windns/PDNS_DNSKEY_DATA, windns/PDNS_KEY_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: windns.h
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
tech.root: 
req.typenames: DNS_KEY_DATA, *PDNS_KEY_DATA, DNS_DNSKEY_DATA, *PDNS_DNSKEY_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windns.h
api_name:
-	DNS_KEY_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DNS_KEY_DATA structure


## -description


The 
<b>DNS_KEY_DATA</b> structure represents a DNS key (KEY) resource record (RR) as specified in <a href=" http://go.microsoft.com/fwlink/p/?linkid=124772">RFC 3445</a>.


## -struct-fields




### -field wFlags

A set of flags that specify whether this is a zone key as  described in section 4 of <a href=" http://go.microsoft.com/fwlink/p/?linkid=124772">RFC 3445</a>.


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
RSA/SHA-1 (<a href="http://go.microsoft.com/fwlink/p/?linkid=90406">RFC 3110</a>). <a href="https://msdn.microsoft.com/5c15980f-6dc7-4b6d-8be1-e22fdea8fe67">DNS_DNSKEY_DATA</a> only.

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

A <b>BYTE</b> array that contains the public key for the algorithm in <b>chAlgorithm</b>, represented in base 64, as described in Appendix A of <a href="http://go.microsoft.com/fwlink/p/?linkid=124775">RFC 2535</a>.


## -remarks



The 
<b>DNS_KEY_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.

The <a href="https://msdn.microsoft.com/5c15980f-6dc7-4b6d-8be1-e22fdea8fe67">DNS_DNSKEY_DATA</a> structure represents a DNSKEY  resource record as specified in section 2 of  <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.

The 
<a href="https://msdn.microsoft.com/5c15980f-6dc7-4b6d-8be1-e22fdea8fe67">DNS_DNSKEY_DATA</a> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.

The value of the <b>wFlags</b> member for <a href="https://msdn.microsoft.com/5c15980f-6dc7-4b6d-8be1-e22fdea8fe67">DNS_DNSKEY_DATA</a> is a set of flags that specify key properties as  described in section 2.1.1 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

