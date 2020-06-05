---
UID: NS:windns._DNS_MESSAGE_BUFFER
title: DNS_MESSAGE_BUFFER (windns.h)
description: The DNS_MESSAGE_BUFFER structure stores message information for DNS queries.helpviewer_keywords: ["*PDNS_MESSAGE_BUFFER","DNS_MESSAGE_BUFFER","DNS_MESSAGE_BUFFER structure [DNS]","PDNS_MESSAGE_BUFFER","PDNS_MESSAGE_BUFFER structure pointer [DNS]","_dns_dns_message_buffer","dns.dns_message_buffer","windns/DNS_MESSAGE_BUFFER","windns/PDNS_MESSAGE_BUFFER"]
old-location: dns\dns_message_buffer.htm
tech.root: DNS
ms.assetid: 2a6fdf8f-ac30-4e32-9cde-67d41ddef8af
ms.date: 12/05/2018
ms.keywords: '*PDNS_MESSAGE_BUFFER, DNS_MESSAGE_BUFFER, DNS_MESSAGE_BUFFER structure [DNS], PDNS_MESSAGE_BUFFER, PDNS_MESSAGE_BUFFER structure pointer [DNS], _dns_dns_message_buffer, dns.dns_message_buffer, windns/DNS_MESSAGE_BUFFER, windns/PDNS_MESSAGE_BUFFER'
f1_keywords:
- windns/DNS_MESSAGE_BUFFER
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
- DNS_MESSAGE_BUFFER
targetos: Windows
req.typenames: DNS_MESSAGE_BUFFER, *PDNS_MESSAGE_BUFFER
req.redist: 
ms.custom: 19H1
---

# DNS_MESSAGE_BUFFER structure


## -description


The 
<b>DNS_MESSAGE_BUFFER</b> structure stores message information for DNS queries.


## -struct-fields




### -field MessageHead

A <a href="https://docs.microsoft.com/windows/desktop/api/windns/ns-windns-dns_header">DNS_HEADER</a> structure that contains the header for the DNS message.


### -field MessageBody

An array of characters that comprises the DNS query or resource records (RR).


## -remarks



The 
<b>DNS_MESSAGE_BUFFER</b> is used by the system to store DNS query information, and make that information available through various DNS function calls.

The <a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnswritequestiontobuffer_utf8">DnsWriteQuestionToBuffer</a> 
	 method should be used to write a DNS query into a <b>DNS_MESSAGE_BUFFER</b> structure and the <a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsextractrecordsfrommessage_utf8">DnsExtractRecordsFromMessage</a> method should be used to read the DNS RRs from a <b>DNS_MESSAGE_BUFFER</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnsextractrecordsfrommessage_utf8">DnsExtractRecordsFromMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windns/nf-windns-dnswritequestiontobuffer_utf8">DnsWriteQuestionToBuffer</a>
 

 

