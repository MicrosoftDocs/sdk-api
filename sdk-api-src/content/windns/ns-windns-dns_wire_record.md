---
UID: NS:windns._DNS_WIRE_RECORD
title: DNS_WIRE_RECORD (windns.h)
description: The DNS_WIRE_RECORD structure contains information about a DNS wire record transmitted across the network as specified in section 4.1.3 of RFC 1035.
helpviewer_keywords: ["*PDNS_WIRE_RECORD","*PDNS_WIRE_RECORD structure [DNS]","DNS_WIRE_RECORD","DNS_WIRE_RECORD structure [DNS]","dns.dns_wire_record","windns/*PDNS_WIRE_RECORD","windns/DNS_WIRE_RECORD"]
old-location: dns\dns_wire_record.htm
tech.root: DNS
ms.assetid: fb36930c-dd43-427a-8034-078c99497a3e
ms.date: 12/05/2018
ms.keywords: '*PDNS_WIRE_RECORD, *PDNS_WIRE_RECORD structure [DNS], DNS_WIRE_RECORD, DNS_WIRE_RECORD structure [DNS], dns.dns_wire_record, windns/*PDNS_WIRE_RECORD, windns/DNS_WIRE_RECORD'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DNS_WIRE_RECORD, *PDNS_WIRE_RECORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DNS_WIRE_RECORD
 - windns/_DNS_WIRE_RECORD
 - PDNS_WIRE_RECORD
 - windns/PDNS_WIRE_RECORD
 - DNS_WIRE_RECORD
 - windns/DNS_WIRE_RECORD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_WIRE_RECORD
---

# DNS_WIRE_RECORD structure


## -description

The <b>DNS_WIRE_RECORD</b> structure contains information about a DNS wire record transmitted across the network as specified in section 4.1.3 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>.

## -struct-fields

### -field RecordType

A value that represents the RR <a href="/windows/desktop/DNS/dns-constants">DNS Response Type</a>. <b>RecordType</b> determines the format of record data that follows the <b>DNS_WIRE_RECORD</b> structure. For example, if the value of <b>RecordType</b> is <b>DNS_TYPE_A</b>, the data type of record data  is <a href="/windows/win32/api/windns/nf-windns-dnsquery_a">DNS_A_DATA</a>.

### -field RecordClass

A value that represents the RR <a href="/windows/desktop/DNS/dns-constants">DNS Record Class</a>.

### -field TimeToLive

The DNS Resource Record's Time To Live value (TTL), in seconds.

### -field DataLength

The length, in bytes, of the DNS record data that follows the <b>DNS_WIRE_RECORD</b>.

## -remarks

When constructing a DNS message, the <b>DNS_WIRE_RECORD</b> structure is immediately followed by the record data and is preceded by the DNS RR's domain name.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/ns-windns-dns_wire_question">DNS_WIRE_QUESTION</a>