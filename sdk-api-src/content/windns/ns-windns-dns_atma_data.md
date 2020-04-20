---
UID: NS:windns.__unnamed_struct_34
title: DNS_ATMA_DATA (windns.h)
description: The DNS_ATMA_DATA structure represents a DNS ATM address (ATMA) resource record (RR).helpviewer_keywords: ["*PDNS_ATMA_DATA","DNS_ATMA_DATA","DNS_ATMA_DATA structure [DNS]","DNS_ATMA_FORMAT_AESA","DNS_ATMA_FORMAT_E164","PDNS_ATMA_DATA","PDNS_ATMA_DATA structure pointer [DNS]","_dns_dns_atma_data","dns.dns_atma_data","windns/DNS_ATMA_DATA","windns/PDNS_ATMA_DATA"]
old-location: dns\dns_atma_data.htm
tech.root: DNS
ms.assetid: 09df3990-36bd-4656-b5cd-792e521adf9d
ms.date: 12/05/2018
ms.keywords: '*PDNS_ATMA_DATA, DNS_ATMA_DATA, DNS_ATMA_DATA structure [DNS], DNS_ATMA_FORMAT_AESA, DNS_ATMA_FORMAT_E164, PDNS_ATMA_DATA, PDNS_ATMA_DATA structure pointer [DNS], _dns_dns_atma_data, dns.dns_atma_data, windns/DNS_ATMA_DATA, windns/PDNS_ATMA_DATA'
f1_keywords:
- windns/DNS_ATMA_DATA
dev_langs:
- c++
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
- DNS_ATMA_DATA
targetos: Windows
req.typenames: DNS_ATMA_DATA, *PDNS_ATMA_DATA
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/windns/ns-windns-dns_recorda">DNS_RECORD</a>
 

 

