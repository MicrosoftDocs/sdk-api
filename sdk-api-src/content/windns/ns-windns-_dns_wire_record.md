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
 

 

