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

# DNS_SIG_DATAA structure


## -description


The <b>DNS_RRSIG_DATA</b> structure represents a DNS
   Security Extensions (DNSSEC) cryptographic signature (SIG) resource  record (RR) as specified in <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


## -struct-fields




### -field wTypeCovered

The <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Record Type</a> of the signed RRs.


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
 


### -field chLabelCount

The number of labels in the original signature RR owner name as specified in section 3.1.3 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


### -field dwOriginalTtl

The Time-to-Live (TTL) value of the RR set signed by <b>Signature</b>.


### -field dwExpiration

The expiration date of <b>Signature</b>, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.


### -field dwTimeSigned

The date and time at which <b>Signature</b> becomes valid, expressed in seconds since the beginning of January 1, 1970, Greenwich Mean Time (GMT), excluding leap seconds.


### -field wKeyTag

A value that represents the method to choose which public key is used to verify  <b>Signature</b> as specified Appendix B of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


### -field wSignatureLength

 


### -field pNameSigner

A pointer to a string that represents  the name of the <b>Signature</b> generator.


### -field size_is

 


### -field size_is.wSignatureLength

 


### -field Signature

A <b>BYTE</b> array that contains the RR set signature as specified in section 3.1.8 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


#### - Pad

Reserved for padding. Do not use.


## -remarks



The 
<b>DNS_RRSIG_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/636399be-43a5-4ddf-b652-f8efb81fbf42">DNS Structures</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

