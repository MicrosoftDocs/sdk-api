---
UID: NF:windns.DnsWriteQuestionToBuffer_W
title: DnsWriteQuestionToBuffer_W function (windns.h)
description: The DnsWriteQuestionToBuffer function type creates a DNS query message and stores it in a DNS_MESSAGE_BUFFER structure. (DnsWriteQuestionToBuffer_W)
helpviewer_keywords: ["DnsWriteQuestionToBuffer","DnsWriteQuestionToBuffer_UTF8","DnsWriteQuestionToBuffer_W","DnsWriteQuestionToBuffer_W function [DNS]","_dns_dnswritequestiontobuffer","dns.dnswritequestiontobuffer","windns/DnsWriteQuestionToBuffer_UTF8","windns/DnsWriteQuestionToBuffer_W"]
old-location: dns\dnswritequestiontobuffer.htm
tech.root: DNS
ms.assetid: 9aa853aa-d9b5-41e3-a82a-c25de199924d
ms.date: 12/05/2018
ms.keywords: DnsWriteQuestionToBuffer, DnsWriteQuestionToBuffer_UTF8, DnsWriteQuestionToBuffer_W, DnsWriteQuestionToBuffer_W function [DNS], _dns_dnswritequestiontobuffer, dns.dnswritequestiontobuffer, windns/DnsWriteQuestionToBuffer_UTF8, windns/DnsWriteQuestionToBuffer_W
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
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsWriteQuestionToBuffer_W
 - windns/DnsWriteQuestionToBuffer_W
dev_langs:
 - c++
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
---

# DnsWriteQuestionToBuffer_W function


## -description

The 
<b>DnsWriteQuestionToBuffer</b> function type creates a DNS query message and stores it in a 
<a href="/windows/desktop/api/windnsdef/ns-windnsdef-dns_message_buffer">DNS_MESSAGE_BUFFER</a> structure. Like many DNS functions, the 
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

A pointer to a <a href="/windows/desktop/api/windnsdef/ns-windnsdef-dns_message_buffer">DNS_MESSAGE_BUFFER</a> structure that contains a DNS query message stored in a buffer.

### -param pdwBufferSize [in, out]

The size, in bytes, of the buffer allocated to store <i>pDnsBuffer</i>. If the buffer size is insufficient to contain the message, <b>FALSE</b> is returned and <i>pdwBufferSize</i> contains the minimum required buffer size.

### -param pszName [in]

A pointer to a string that represents the name of the owner of the record set being queried.

### -param wType [in]

A value that represents the RR <a href="/windows/desktop/DNS/dns-constants">DNS Record Type</a>. <b>wType</b> determines the format of <b>Data</b>. For example, if the value of <b>wType</b> is <b>DNS_TYPE_A</b>, the data type of <b>Data</b> is <a href="/windows/win32/api/windns/nf-windns-dnsquery_a">DNS_A_DATA</a>.

### -param Xid [in]

A value that specifies the unique DNS query identifier.

### -param fRecursionDesired [in]

A BOOL that specifies whether recursive name query should be used  by the DNS name server. Set to <b>TRUE</b> to request recursive name query, <b>FALSE</b> to request iterative name query.

## -returns

Returns <b>TRUE</b> upon successful execution, otherwise <b>FALSE</b>.

## -remarks

The following declaration for <b>DnsWriteQuestionToBuffer_UTF8</b> can be found in Windns.h.


``` syntax
BOOL
WINAPI
DnsWriteQuestionToBuffer_UTF8(
    __inout     PDNS_MESSAGE_BUFFER pDnsBuffer,
    __inout     PDWORD              pdwBufferSize,
    __in        PCSTR               pszName,
    __in        WORD                wType,
    __in        WORD                Xid,
    __in        BOOL                fRecursionDesired
    );
```


## -see-also

<a href="/windows/desktop/api/windnsdef/ns-windnsdef-dns_message_buffer">DNS_MESSAGE_BUFFER</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>
