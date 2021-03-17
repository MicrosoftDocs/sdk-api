---
UID: NC:windns.DNS_QUERY_COMPLETION_ROUTINE
title: DNS_QUERY_COMPLETION_ROUTINE (windns.h)
description: The DNS_QUERY_COMPLETION_ROUTINE callback is used to asynchronously return the results of a DNS query.
helpviewer_keywords: ["DNS_QUERY_COMPLETION_ROUTINE","DNS_QUERY_COMPLETION_ROUTINE callback","DNS_QUERY_COMPLETION_ROUTINE callback function [DNS]","dns.dns_query_completion_routine","windns/DNS_QUERY_COMPLETION_ROUTINE"]
old-location: dns\dns_query_completion_routine.htm
tech.root: DNS
ms.assetid: 35D78208-FFC1-48B0-8267-EE583DE2D783
ms.date: 12/05/2018
ms.keywords: DNS_QUERY_COMPLETION_ROUTINE, DNS_QUERY_COMPLETION_ROUTINE callback, DNS_QUERY_COMPLETION_ROUTINE callback function [DNS], dns.dns_query_completion_routine, windns/DNS_QUERY_COMPLETION_ROUTINE
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DNS_QUERY_COMPLETION_ROUTINE
 - windns/DNS_QUERY_COMPLETION_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Windns.h
api_name:
 - DNS_QUERY_COMPLETION_ROUTINE
---

# DNS_QUERY_COMPLETION_ROUTINE callback function


## -description

The <b>DNS_QUERY_COMPLETION_ROUTINE</b> callback is used to asynchronously return the results of a DNS query.

## -parameters

### -param pQueryContext [in]

A pointer to a user context.

### -param pQueryResults [in, out]

A pointer to a <a href="/windows/desktop/api/windns/ns-windns-dns_query_result">DNS_QUERY_RESULT</a> structure that contains the DNS query results from a call to <a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>.

## -see-also

<a href="/windows/desktop/api/windns/ns-windns-dns_query_cancel">DNS_QUERY_CANCEL</a>



<a href="/windows/desktop/api/windns/ns-windns-dns_query_request">DNS_QUERY_REQUEST</a>



<a href="/windows/desktop/api/windns/ns-windns-dns_query_result">DNS_QUERY_RESULT</a>



<a href="/windows/desktop/api/windns/nf-windns-dnscancelquery">DnsCancelQuery</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>