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

# DnsExtractRecordsFromMessage_W function


## -description


The 
<b>DnsExtractRecordsFromMessage</b> function type extracts resource records (RR) from a DNS message, and stores those records in a 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure. Like many DNS functions, the 
<b>DnsExtractRecordsFromMessage</b> function type is implemented in multiple forms to facilitate different character encoding. Based on the character encoding involved, use one of the following functions:
<ul>
<li>
<b>DnsExtractRecordsFromMessage_W</b> (_W for Unicode encoding)

</li>
<li>
<b>DnsExtractRecordsFromMessage_UTF8</b> (_UTF8 for UTF-8 encoding)

</li>
</ul>If the 
<b>DnsExtractRecordsFromMessage</b> function type is used without its suffix (either _W or _UTF8), a compiler error will occur.


## -parameters




### -param pDnsBuffer [in]

A pointer to a <a href="https://msdn.microsoft.com/2a6fdf8f-ac30-4e32-9cde-67d41ddef8af">DNS_MESSAGE_BUFFER</a> structure that contains the DNS response message.


### -param wMessageLength [in]

The size, in bytes, of the message in 
<i>pDnsBuffer</i>.


### -param ppRecord [out]

A pointer to a <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the list of extracted RRs. To free these records, use the 
<a href="https://msdn.microsoft.com/fc4c0cb4-646f-4946-8f07-b5a858f7064a">DnsRecordListFree</a> function.


## -returns



Returns success confirmation upon successful completion. Otherwise, returns the appropriate DNS-specific error code as defined in Winerror.h.




## -remarks



The <b>DnsExtractRecordsFromMessage</b> function is designed to operate on messages in host byte order. As such, received messages should be converted from network byte order to host byte order before extraction, or before retransmission onto the network. Use the DNS_BYTE_FLIP_HEADER_COUNTS macro to change  byte ordering.

The following declaration for <b>DnsExtractRecordsFromMessage_UTF8</b> can be found in Windns.h.

<pre class="syntax" xml:space="preserve"><code>DNS_STATUS
WINAPI
DnsExtractRecordsFromMessage_UTF8(
    __in            PDNS_MESSAGE_BUFFER pDnsBuffer,
    __in            WORD                wMessageLength,
    __deref_out     PDNS_RECORD *       ppRecord
    );
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/2a6fdf8f-ac30-4e32-9cde-67d41ddef8af">DNS_MESSAGE_BUFFER</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a>



<a href="https://msdn.microsoft.com/fc4c0cb4-646f-4946-8f07-b5a858f7064a">DnsRecordListFree</a>



<a href="https://msdn.microsoft.com/9aa853aa-d9b5-41e3-a82a-c25de199924d">DnsWriteQuestionToBuffer</a>
 

 

