---
UID: NS:windns._DNS_WIRE_QUESTION
title: "_DNS_WIRE_QUESTION"
author: windows-sdk-content
description: The DNS_WIRE_QUESTION structure contains information about a DNS question transmitted across the network as specified in section 4.1.2 of RFC 1035..
old-location: dns\dns_wire_question.htm
old-project: dns
ms.assetid: 50498f20-0896-4471-8355-edd997aa4bcd
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PDNS_WIRE_QUESTION, *PDNS_WIRE_QUESTION structure [DNS], DNS_WIRE_QUESTION, DNS_WIRE_QUESTION structure [DNS], _DNS_WIRE_QUESTION, dns.dns_wire_question, windns/*PDNS_WIRE_QUESTION, windns/DNS_WIRE_QUESTION"
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
req.typenames: DNS_WIRE_QUESTION, *PDNS_WIRE_QUESTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_WIRE_QUESTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DNS_WIRE_QUESTION structure


## -description


The <b>DNS_WIRE_QUESTION</b> structure contains information about a DNS question transmitted across the network as specified in section 4.1.2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=90264">RFC 1035</a>..


## -struct-fields




### -field QuestionType

A value that represents the question section's <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Question Type</a>.


### -field QuestionClass

A value that represents the question section's <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Question Class</a>.


## -remarks



When constructing a DNS message, the question name must precede the <b>DNS_WIRE_QUESTION</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/fb36930c-dd43-427a-8034-078c99497a3e">DNS_WIRE_RECORD</a>
 

 

