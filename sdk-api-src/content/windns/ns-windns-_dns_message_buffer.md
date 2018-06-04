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
 

 

