---
UID: NS:windns._DNS_QUERY_REQUEST
title: DNS_QUERY_REQUEST (windns.h)
description: The DNS_QUERY_REQUEST structure contains the DNS query parameters used in a call to DnsQueryEx.
helpviewer_keywords: ["*PDNS_QUERY_REQUEST","DNS_QUERY_REQUEST","DNS_QUERY_REQUEST structure [DNS]","DNS_QUERY_REQUEST_VERSION1","PDNS_QUERY_REQUEST","PDNS_QUERY_REQUEST structure pointer [DNS]","dns.dns_query_request","windns/DNS_QUERY_REQUEST","windns/PDNS_QUERY_REQUEST"]
old-location: dns\dns_query_request.htm
tech.root: DNS
ms.assetid: 9C382800-DE71-4481-AC8D-9F89D6F59EE6
ms.date: 12/05/2018
ms.keywords: '*PDNS_QUERY_REQUEST, DNS_QUERY_REQUEST, DNS_QUERY_REQUEST structure [DNS], DNS_QUERY_REQUEST_VERSION1, PDNS_QUERY_REQUEST, PDNS_QUERY_REQUEST structure pointer [DNS], dns.dns_query_request, windns/DNS_QUERY_REQUEST, windns/PDNS_QUERY_REQUEST'
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
req.typenames: DNS_QUERY_REQUEST, *PDNS_QUERY_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DNS_QUERY_REQUEST
 - windns/_DNS_QUERY_REQUEST
 - PDNS_QUERY_REQUEST
 - windns/PDNS_QUERY_REQUEST
 - DNS_QUERY_REQUEST
 - windns/DNS_QUERY_REQUEST
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
 - DNS_QUERY_REQUEST
---

# DNS_QUERY_REQUEST structure


## -description

The <b>DNS_QUERY_REQUEST</b> structure contains the DNS query parameters used in a call to <a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>.

## -struct-fields

### -field Version

The structure version must be one of the following:



#### DNS_QUERY_REQUEST_VERSION1 (1)

### -field QueryName

A pointer to a string that represents the DNS name to query.

<div class="alert"><b>Note</b>  If <b>QueryName</b> is NULL, the query is for the local machine name.</div>
<div> </div>

### -field QueryType

A value that represents the Resource Record (RR) <a href="/windows/desktop/DNS/dns-constants">DNS Record Type</a> that is queried. <b>QueryType</b> determines the format of data pointed to by <b>pQueryRecords</b> returned in the <a href="/windows/desktop/api/windns/ns-windns-dns_query_result">DNS_QUERY_RESULT</a> structure. For example, if the value of <b>wType</b> is <b>DNS_TYPE_A</b>, the format of data pointed to by <b>pQueryRecords</b> is <a href="/windows/win32/api/windns/nf-windns-dnsquery_a">DNS_A_DATA</a>.

### -field QueryOptions

A value that contains a bitmap of <a href="/windows/desktop/DNS/dns-constants">DNS Query  Options</a> to use in the DNS query. Options can be combined and all options override <b>DNS_QUERY_STANDARD</b>

### -field pDnsServerList

A pointer to a <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_addr_array">DNS_ADDR_ARRAY</a> structure that contains a list of DNS servers to use in the query.

### -field InterfaceIndex

A value that contains the interface index over which the query is sent. If <b>InterfaceIndex</b> is 0, all interfaces will be considered.

### -field pQueryCompletionCallback

A pointer to a <a href="/windows/desktop/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> callback that is used to return the results of an asynchronous query from a  call to <a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>.

<div class="alert"><b>Note</b>  If NULL, <a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a> is called synchronously.</div>
<div> </div>

### -field pQueryContext

A pointer to a user context.

## -see-also

<a href="/windows/desktop/api/windns/ns-windns-dns_query_cancel">DNS_QUERY_CANCEL</a>



<a href="/windows/desktop/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a>



<a href="/windows/desktop/api/windns/ns-windns-dns_query_result">DNS_QUERY_RESULT</a>



<a href="/windows/desktop/api/windns/nf-windns-dnscancelquery">DnsCancelQuery</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>