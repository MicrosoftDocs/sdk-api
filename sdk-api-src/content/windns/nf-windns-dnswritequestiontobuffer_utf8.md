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
 

 

