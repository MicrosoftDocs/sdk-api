---
UID: NS:windns._DNS_WIRE_RECORD
title: "_DNS_WIRE_RECORD"
author: windows-sdk-content
description: The DNS_WIRE_RECORD structure contains information about a DNS wire record transmitted across the network as specified in section 4.1.3 of RFC 1035.
old-location: dns\dns_wire_record.htm
old-project: dns
ms.assetid: fb36930c-dd43-427a-8034-078c99497a3e
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PDNS_WIRE_RECORD, *PDNS_WIRE_RECORD structure [DNS], DNS_WIRE_RECORD, DNS_WIRE_RECORD structure [DNS], _DNS_WIRE_RECORD, dns.dns_wire_record, windns/*PDNS_WIRE_RECORD, windns/DNS_WIRE_RECORD"
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
req.typenames: DNS_WIRE_RECORD, *PDNS_WIRE_RECORD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_WIRE_RECORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DNS_WIRE_RECORD structure


## -description


The <b>DNS_WIRE_RECORD</b> structure contains information about a DNS wire record transmitted across the network as specified in section 4.1.3 of <a href="http://go.microsoft.com/fwlink/p/?linkid=90264">RFC 1035</a>.


## -struct-fields




### -field RecordType

A value that represents the RR <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Response Type</a>. <b>RecordType</b> determines the format of record data that follows the <b>DNS_WIRE_RECORD</b> structure. For example, if the value of <b>RecordType</b> is <b>DNS_TYPE_A</b>, the data type of record data  is <a href="https://msdn.microsoft.com/0fd21930-1319-4ae7-b46f-2b744f4faae9">DNS_A_DATA</a>.


### -field RecordClass

A value that represents the RR <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Record Class</a>.


### -field TimeToLive

The DNS Resource Record's Time To Live value (TTL), in seconds.


### -field DataLength

The length, in bytes, of the DNS record data that follows the <b>DNS_WIRE_RECORD</b>.


## -remarks



When constructing a DNS message, the <b>DNS_WIRE_RECORD</b> structure is immediately followed by the record data and is preceded by the DNS RR's domain name.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/50498f20-0896-4471-8355-edd997aa4bcd">DNS_WIRE_QUESTION</a>
 

 

