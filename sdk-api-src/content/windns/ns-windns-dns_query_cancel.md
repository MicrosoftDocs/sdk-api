---
UID: NS:windns._DNS_QUERY_CANCEL
title: DNS_QUERY_CANCEL (windns.h)
description: A DNS_QUERY_CANCEL structure can be used to cancel an asynchronous DNS query.
helpviewer_keywords: ["*PDNS_QUERY_CANCEL","DNS_QUERY_CANCEL","DNS_QUERY_CANCEL structure [DNS]","PDNS_QUERY_CANCEL","PDNS_QUERY_CANCEL structure pointer [DNS]","dns.dns_query_cancel","windns/DNS_QUERY_CANCEL","windns/PDNS_QUERY_CANCEL"]
old-location: dns\dns_query_cancel.htm
tech.root: DNS
ms.assetid: 543C6F9B-3200-44F6-A2B7-A5C7F5A927DB
ms.date: 12/05/2018
ms.keywords: '*PDNS_QUERY_CANCEL, DNS_QUERY_CANCEL, DNS_QUERY_CANCEL structure [DNS], PDNS_QUERY_CANCEL, PDNS_QUERY_CANCEL structure pointer [DNS], dns.dns_query_cancel, windns/DNS_QUERY_CANCEL, windns/PDNS_QUERY_CANCEL'
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: DNS_QUERY_CANCEL, *PDNS_QUERY_CANCEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DNS_QUERY_CANCEL
 - windns/_DNS_QUERY_CANCEL
 - PDNS_QUERY_CANCEL
 - windns/PDNS_QUERY_CANCEL
 - DNS_QUERY_CANCEL
 - windns/DNS_QUERY_CANCEL
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
 - DNS_QUERY_CANCEL
---

# DNS_QUERY_CANCEL structure


## -description

A <b>DNS_QUERY_CANCEL</b> structure can be used to cancel an asynchronous DNS query.

## -struct-fields

### -field Reserved

Contains a handle to the asynchronous query to cancel. Applications must not modify this value.

## -remarks

This structure is returned in the <i>pCancelHandle</i> parameter from a previous call to <a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>.

## -see-also

<a href="/windows/desktop/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a>



<a href="/windows/desktop/api/windns/ns-windns-dns_query_request">DNS_QUERY_REQUEST</a>



<a href="/windows/desktop/api/windns/ns-windns-dns_query_result">DNS_QUERY_RESULT</a>