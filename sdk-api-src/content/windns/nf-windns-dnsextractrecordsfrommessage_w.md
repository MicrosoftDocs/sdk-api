---
UID: NF:windns.DnsExtractRecordsFromMessage_W
title: DnsExtractRecordsFromMessage_W function (windns.h)
description: The DnsExtractRecordsFromMessage function type extracts resource records (RR) from a DNS message, and stores those records in a DNS_RECORD structure. (DnsExtractRecordsFromMessage_W)
helpviewer_keywords: ["DnsExtractRecordsFromMessage","DnsExtractRecordsFromMessage_UTF8","DnsExtractRecordsFromMessage_W","DnsExtractRecordsFromMessage_W function [DNS]","_dns_dnsextractrecordsfrommessage","dns.dnsextractrecordsfrommessage","windns/DnsExtractRecordsFromMessage_UTF8","windns/DnsExtractRecordsFromMessage_W"]
old-location: dns\dnsextractrecordsfrommessage.htm
tech.root: DNS
ms.assetid: 0179bf3e-9243-4dd7-a2ab-e2f6f4bf4b82
ms.date: 12/05/2018
ms.keywords: DnsExtractRecordsFromMessage, DnsExtractRecordsFromMessage_UTF8, DnsExtractRecordsFromMessage_W, DnsExtractRecordsFromMessage_W function [DNS], _dns_dnsextractrecordsfrommessage, dns.dnsextractrecordsfrommessage, windns/DnsExtractRecordsFromMessage_UTF8, windns/DnsExtractRecordsFromMessage_W
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
 - DnsExtractRecordsFromMessage_W
 - windns/DnsExtractRecordsFromMessage_W
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
 - DnsExtractRecordsFromMessage_W
 - DnsExtractRecordsFromMessage_UTF8
---

# DnsExtractRecordsFromMessage_W function


## -description

The 
<b>DnsExtractRecordsFromMessage</b> function type extracts resource records (RR) from a DNS message, and stores those records in a 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure. Like many DNS functions, the 
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

A pointer to a <a href="/windows/desktop/api/windnsdef/ns-windnsdef-dns_message_buffer">DNS_MESSAGE_BUFFER</a> structure that contains the DNS response message.

### -param wMessageLength [in]

The size, in bytes, of the message in 
<i>pDnsBuffer</i>.

### -param ppRecord [out]

A pointer to a <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure that contains the list of extracted RRs. To free these records, use the 
<a href="/windows/desktop/api/windns/nf-windns-dnsrecordlistfree">DnsRecordListFree</a> function.

## -returns

Returns success confirmation upon successful completion. Otherwise, returns the appropriate DNS-specific error code as defined in Winerror.h.

## -remarks

The <b>DnsExtractRecordsFromMessage</b> function is designed to operate on messages in host byte order. As such, received messages should be converted from network byte order to host byte order before extraction, or before retransmission onto the network. Use the DNS_BYTE_FLIP_HEADER_COUNTS macro to change  byte ordering.

The following declaration for <b>DnsExtractRecordsFromMessage_UTF8</b> can be found in Windns.h.


``` syntax
DNS_STATUS
WINAPI
DnsExtractRecordsFromMessage_UTF8(
    __in            PDNS_MESSAGE_BUFFER pDnsBuffer,
    __in            WORD                wMessageLength,
    __deref_out     PDNS_RECORD *       ppRecord
    );

```


## -see-also

<a href="/windows/desktop/api/windnsdef/ns-windnsdef-dns_message_buffer">DNS_MESSAGE_BUFFER</a>



<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsrecordlistfree">DnsRecordListFree</a>



<a href="/windows/desktop/api/windns/nf-windns-dnswritequestiontobuffer_utf8">DnsWriteQuestionToBuffer</a>
