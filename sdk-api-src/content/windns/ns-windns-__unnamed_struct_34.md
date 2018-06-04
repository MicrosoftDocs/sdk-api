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

# DNS_ATMA_DATA structure


## -description


The 
<b>DNS_ATMA_DATA</b> structure represents a DNS ATM address (ATMA) resource record (RR).


## -struct-fields




### -field AddressType

The format of the ATM address in <b>Address</b>. The possible values for <b>AddressType</b> are: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DNS_ATMA_FORMAT_AESA"></a><a id="dns_atma_format_aesa"></a><dl>
<dt><b>DNS_ATMA_FORMAT_AESA</b></dt>
</dl>
</td>
<td width="60%">
An address of the form: 39.246f.123456789abcdefa0123.00123456789a.00. It is a 40 hex character address mapped to 20 octets with arbitrarily placed "." separators. Its length is exactly <b>DNS_ATMA_AESA_ADDR_LENGTH</b> bytes. 

</td>
</tr>
<tr>
<td width="40%"><a id="DNS_ATMA_FORMAT_E164"></a><a id="dns_atma_format_e164"></a><dl>
<dt><b>DNS_ATMA_FORMAT_E164</b></dt>
</dl>
</td>
<td width="60%">
An address of the form: +358.400.1234567\0.  The null-terminated hex characters map one-to-one into the ATM address
    with arbitrarily placed "." separators. The '+' indicates it is an E.164 format address. Its length is less than <b>DNS_ATMA_MAX_ADDR_LENGTH</b> bytes.

</td>
</tr>
</table>
 


### -field Address

A <b>BYTE</b> array that contains the ATM address whose format is specified by <b>AddressType</b>.


## -remarks



The 
<b>DNS_ATMA_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

