---
UID: NS:windns.__unnamed_struct_18
title: DNS_KEY_DATA
author: windows-driver-content
description: RFC 4034.
old-location: dns\dns_dnskey_data.htm
old-project: DNS
ms.assetid: 5c15980f-6dc7-4b6d-8be1-e22fdea8fe67
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: "*PDNS_DNSKEY_DATA, *PDNS_KEY_DATA, 1, 2, 3, 4, 5, DNS_DNSKEY_DATA, DNS_DNSKEY_DATA structure [DNS], DNS_KEY_DATA, PDNS_DNSKEY_DATA, PDNS_DNSKEY_DATA structure pointer [DNS], dns.dns_dnskey_data, windns/DNS_DNSKEY_DATA, windns/PDNS_DNSKEY_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DNS_KEY_DATA, *PDNS_KEY_DATA, DNS_DNSKEY_DATA, *PDNS_DNSKEY_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windns.h
api_name:
-	DNS_DNSKEY_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DNS_KEY_DATA structure


## -description


The <b>DNS_DNSKEY_DATA</b> structure represents a DNSKEY  resource record as specified in section 2 of  <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


## -struct-fields




### -field wFlags

A set of flags that specify key properties as  described in section 2.1.1 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


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
RSA/SHA-1 (<a href="http://go.microsoft.com/fwlink/p/?linkid=90406">RFC 3110</a>)

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

A BYTE array that contains the public key for the algorithm specified in <b>chAlgorithm</b>. Its length is determined by <b>wKeyLength</b>.


## -remarks



The 
<b>DNS_DNSKEY_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/636399be-43a5-4ddf-b652-f8efb81fbf42">DNS Structures</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

