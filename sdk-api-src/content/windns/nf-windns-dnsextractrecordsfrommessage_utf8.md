---
UID: NF:windns.DnsExtractRecordsFromMessage_UTF8
title: DnsExtractRecordsFromMessage_UTF8 function
author: windows-sdk-content
description: The DnsExtractRecordsFromMessage function type extracts resource records (RR) from a DNS message, and stores those records in a DNS_RECORD structure.
old-location: dns\dnsextractrecordsfrommessage.htm
old-project: DNS
ms.assetid: 0179bf3e-9243-4dd7-a2ab-e2f6f4bf4b82
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: DnsExtractRecordsFromMessage, DnsExtractRecordsFromMessage_UTF8, DnsExtractRecordsFromMessage_W, DnsExtractRecordsFromMessage_W function [DNS], _dns_dnsextractrecordsfrommessage, dns.dnsextractrecordsfrommessage, windns/DnsExtractRecordsFromMessage_UTF8, windns/DnsExtractRecordsFromMessage_W
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: DNS_FREE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsExtractRecordsFromMessage_W
 - DnsExtractRecordsFromMessage_UTF8
product: Windows
targetos: Windows
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DnsExtractRecordsFromMessage_UTF8 function


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
 

 

