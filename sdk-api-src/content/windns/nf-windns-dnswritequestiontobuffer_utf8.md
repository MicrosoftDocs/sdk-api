---
UID: NF:windns.DnsWriteQuestionToBuffer_UTF8
title: DnsWriteQuestionToBuffer_UTF8 function
author: windows-sdk-content
description: The DnsWriteQuestionToBuffer function type creates a DNS query message and stores it in a DNS_MESSAGE_BUFFER structure.
old-location: dns\dnswritequestiontobuffer.htm
old-project: DNS
ms.assetid: 9aa853aa-d9b5-41e3-a82a-c25de199924d
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: DnsWriteQuestionToBuffer, DnsWriteQuestionToBuffer_UTF8, DnsWriteQuestionToBuffer_W, DnsWriteQuestionToBuffer_W function [DNS], _dns_dnswritequestiontobuffer, dns.dnswritequestiontobuffer, windns/DnsWriteQuestionToBuffer_UTF8, windns/DnsWriteQuestionToBuffer_W
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
 - DnsWriteQuestionToBuffer_W
 - DnsWriteQuestionToBuffer_UTF8
product: Windows
targetos: Windows
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DnsWriteQuestionToBuffer_UTF8 function


## -description


The 
<b>DnsWriteQuestionToBuffer</b> function type creates a DNS query message and stores it in a 
<a href="https://msdn.microsoft.com/2a6fdf8f-ac30-4e32-9cde-67d41ddef8af">DNS_MESSAGE_BUFFER</a> structure. Like many DNS functions, the 
<b>DnsWriteQuestionToBuffer</b> function type is implemented in multiple forms to facilitate different character encoding. Based on the character encoding involved, use one of the following functions:
<ul>
<li>
<b>DnsWriteQuestionToBuffer_W</b> (_W for Unicode encoding)

</li>
<li>
<b>DnsWriteQuestionToBuffer_UTF8</b> (_UTF8 for UTF-8 encoding)

</li>
</ul>If the 
<b>DnsWriteQuestionToBuffer</b> function type is used without its suffix (either _W or _UTF8), a compiler error will occur.


## -parameters




### -param pDnsBuffer [in, out]

A pointer to a <a href="https://msdn.microsoft.com/2a6fdf8f-ac30-4e32-9cde-67d41ddef8af">DNS_MESSAGE_BUFFER</a> structure that contains a DNS query message stored in a buffer.


### -param pdwBufferSize [in, out]

The size, in bytes, of the buffer allocated to store <i>pDnsBuffer</i>. If the buffer size is insufficient to contain the message, <b>FALSE</b> is returned and <i>pdwBufferSize</i> contains the minimum required buffer size.


### -param pszName [in]

A pointer to a string that represents the name of the owner of the record set being queried.


### -param wType [in]

A value that represents the RR <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Record Type</a>. <b>wType</b> determines the format of <b>Data</b>. For example, if the value of <b>wType</b> is <b>DNS_TYPE_A</b>, the data type of <b>Data</b> is <a href="https://msdn.microsoft.com/0fd21930-1319-4ae7-b46f-2b744f4faae9">DNS_A_DATA</a>.


### -param Xid [in]

A value that specifies the unique DNS query identifier.


### -param fRecursionDesired [in]

A BOOL that specifies whether recursive name query should be used  by the DNS name server. Set to <b>TRUE</b> to request recursive name query, <b>FALSE</b> to request iterative name query.


## -returns



Returns <b>TRUE</b> upon successful execution, otherwise <b>FALSE</b>.




## -remarks



The following declaration for <b>DnsWriteQuestionToBuffer_UTF8</b> can be found in Windns.h.

<pre class="syntax" xml:space="preserve"><code>BOOL
WINAPI
DnsWriteQuestionToBuffer_UTF8(
    __inout     PDNS_MESSAGE_BUFFER pDnsBuffer,
    __inout     PDWORD              pdwBufferSize,
    __in        PCSTR               pszName,
    __in        WORD                wType,
    __in        WORD                Xid,
    __in        BOOL                fRecursionDesired
    );</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/2a6fdf8f-ac30-4e32-9cde-67d41ddef8af">DNS_MESSAGE_BUFFER</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a>
 

 

