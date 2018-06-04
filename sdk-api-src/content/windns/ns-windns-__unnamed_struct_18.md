---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

