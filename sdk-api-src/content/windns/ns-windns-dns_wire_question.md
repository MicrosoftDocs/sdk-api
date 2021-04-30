---
UID: NS:windns._DNS_WIRE_QUESTION
title: DNS_WIRE_QUESTION (windns.h)
description: The DNS_WIRE_QUESTION structure contains information about a DNS question transmitted across the network as specified in section 4.1.2 of RFC 1035..
helpviewer_keywords: ["*PDNS_WIRE_QUESTION","*PDNS_WIRE_QUESTION structure [DNS]","DNS_WIRE_QUESTION","DNS_WIRE_QUESTION structure [DNS]","dns.dns_wire_question","windns/*PDNS_WIRE_QUESTION","windns/DNS_WIRE_QUESTION"]
old-location: dns\dns_wire_question.htm
tech.root: DNS
ms.assetid: 50498f20-0896-4471-8355-edd997aa4bcd
ms.date: 12/05/2018
ms.keywords: '*PDNS_WIRE_QUESTION, *PDNS_WIRE_QUESTION structure [DNS], DNS_WIRE_QUESTION, DNS_WIRE_QUESTION structure [DNS], dns.dns_wire_question, windns/*PDNS_WIRE_QUESTION, windns/DNS_WIRE_QUESTION'
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
req.typenames: DNS_WIRE_QUESTION, *PDNS_WIRE_QUESTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DNS_WIRE_QUESTION
 - windns/_DNS_WIRE_QUESTION
 - PDNS_WIRE_QUESTION
 - windns/PDNS_WIRE_QUESTION
 - DNS_WIRE_QUESTION
 - windns/DNS_WIRE_QUESTION
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
 - DNS_WIRE_QUESTION
---

# DNS_WIRE_QUESTION structure


## -description

The <b>DNS_WIRE_QUESTION</b> structure contains information about a DNS question transmitted across the network as specified in section 4.1.2 of <a href="https://www.ietf.org/rfc/rfc1035.txt">RFC 1035</a>..

## -struct-fields

### -field QuestionType

A value that represents the question section's <a href="/windows/desktop/DNS/dns-constants">DNS Question Type</a>.

### -field QuestionClass

A value that represents the question section's <a href="/windows/desktop/DNS/dns-constants">DNS Question Class</a>.

## -remarks

When constructing a DNS message, the question name must precede the <b>DNS_WIRE_QUESTION</b> structure.

## -see-also

<a href="/windows/desktop/api/windns/ns-windns-dns_wire_record">DNS_WIRE_RECORD</a>