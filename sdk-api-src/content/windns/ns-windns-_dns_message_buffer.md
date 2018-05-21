---
UID: NS:windns._DNS_MESSAGE_BUFFER
title: "_DNS_MESSAGE_BUFFER"
author: windows-driver-content
description: The DNS_MESSAGE_BUFFER structure stores message information for DNS queries.
old-location: dns\dns_message_buffer.htm
old-project: DNS
ms.assetid: 2a6fdf8f-ac30-4e32-9cde-67d41ddef8af
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: "*PDNS_MESSAGE_BUFFER, DNS_MESSAGE_BUFFER, DNS_MESSAGE_BUFFER structure [DNS], PDNS_MESSAGE_BUFFER, PDNS_MESSAGE_BUFFER structure pointer [DNS], _DNS_MESSAGE_BUFFER, _dns_dns_message_buffer, dns.dns_message_buffer, windns/DNS_MESSAGE_BUFFER, windns/PDNS_MESSAGE_BUFFER"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DNS_MESSAGE_BUFFER, *PDNS_MESSAGE_BUFFER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windns.h
api_name:
-	DNS_MESSAGE_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DNS_MESSAGE_BUFFER structure


## -description


The 
<b>DNS_MESSAGE_BUFFER</b> structure stores message information for DNS queries.


## -struct-fields




### -field MessageHead

A <a href="https://msdn.microsoft.com/e5bf19a1-4c71-482d-a075-1e149f94505b">DNS_HEADER</a> structure that contains the header for the DNS message.


### -field MessageBody

An array of characters that comprises the DNS query or resource records (RR).


## -remarks



The 
<b>DNS_MESSAGE_BUFFER</b> is used by the system to store DNS query information, and make that information available through various DNS function calls.

The <a href="https://msdn.microsoft.com/9aa853aa-d9b5-41e3-a82a-c25de199924d">DnsWriteQuestionToBuffer</a> 
	 method should be used to write a DNS query into a <b>DNS_MESSAGE_BUFFER</b> structure and the <a href="https://msdn.microsoft.com/0179bf3e-9243-4dd7-a2ab-e2f6f4bf4b82">DnsExtractRecordsFromMessage</a> method should be used to read the DNS RRs from a <b>DNS_MESSAGE_BUFFER</b>.




## -see-also




<a href="https://msdn.microsoft.com/0179bf3e-9243-4dd7-a2ab-e2f6f4bf4b82">DnsExtractRecordsFromMessage</a>



<a href="https://msdn.microsoft.com/9aa853aa-d9b5-41e3-a82a-c25de199924d">DnsWriteQuestionToBuffer</a>
 

 

