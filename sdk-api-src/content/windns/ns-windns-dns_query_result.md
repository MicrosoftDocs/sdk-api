---
UID: NS:windns._DNS_QUERY_RESULT
title: DNS_QUERY_RESULT (windns.h)
description: A DNS_QUERY_RESULT structure contains the DNS query results returned from a call to DnsQueryEx.
helpviewer_keywords: ["*PDNS_QUERY_RESULT","DNS_QUERY_REQUEST_VERSION1","DNS_QUERY_RESULT","DNS_QUERY_RESULT structure [DNS]","PDNS_QUERY_RESULT","PDNS_QUERY_RESULT structure pointer [DNS]","dns.dns_query_result","windns/DNS_QUERY_RESULT","windns/PDNS_QUERY_RESULT"]
old-location: dns\dns_query_result.htm
tech.root: DNS
ms.assetid: 03EB1DC2-FAB0-45C5-B438-E8FFDD218F09
ms.date: 12/05/2018
ms.keywords: '*PDNS_QUERY_RESULT, DNS_QUERY_REQUEST_VERSION1, DNS_QUERY_RESULT, DNS_QUERY_RESULT structure [DNS], PDNS_QUERY_RESULT, PDNS_QUERY_RESULT structure pointer [DNS], dns.dns_query_result, windns/DNS_QUERY_RESULT, windns/PDNS_QUERY_RESULT'
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
req.typenames: DNS_QUERY_RESULT, *PDNS_QUERY_RESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DNS_QUERY_RESULT
 - windns/_DNS_QUERY_RESULT
 - PDNS_QUERY_RESULT
 - windns/PDNS_QUERY_RESULT
 - DNS_QUERY_RESULT
 - windns/DNS_QUERY_RESULT
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
 - DNS_QUERY_RESULT
---

# DNS_QUERY_RESULT structure


## -description

A <b>DNS_QUERY_RESULT</b>  structure contains the DNS query results returned from a call to <a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>.

## -struct-fields

### -field Version

The structure version must be one of the following:



#### DNS_QUERY_REQUEST_VERSION1 (1)

### -field QueryStatus

The return status of the call to <a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>. 

If the query was completed asynchronously and this structure was returned directly from <a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>, <b>QueryStatus</b> contains <b>DNS_REQUEST_PENDING</b>.

If the query was completed synchronously or if this structure was returned by the <a href="/windows/desktop/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> DNS callback, <b>QueryStatus</b> contains ERROR_SUCCESS if successful or the appropriate DNS-specific error code as defined in Winerror.h.

### -field QueryOptions

A value that contains a bitmap of <a href="/windows/desktop/DNS/dns-constants">DNS Query  Options</a> that were used in the DNS query. Options can be combined and all options override <b>DNS_QUERY_STANDARD</b>

### -field pQueryRecords

A pointer to a <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure.

If the query was completed asynchronously and this structure was returned directly from <a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>, <b>pQueryRecords</b> is NULL.

If the query was completed synchronously or if this structure was returned by the <a href="/windows/desktop/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> DNS callback, <b>pQueryRecords</b> contains a list of Resource Records (RR) that comprise the response.

<div class="alert"><b>Note</b>  Applications must free returned RR sets with the <a href="/windows/desktop/api/windns/nf-windns-dnsrecordlistfree">DnsRecordListFree</a> function.</div>
<div> </div>

### -field Reserved

### -field reserved

This value is reserved for future use and must be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/windns/ns-windns-dns_query_cancel">DNS_QUERY_CANCEL</a>



<a href="/windows/desktop/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a>



<a href="/windows/desktop/api/windns/ns-windns-dns_query_request">DNS_QUERY_REQUEST</a>