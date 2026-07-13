---
UID: NF:windns.DnsQuery_A
title: DnsQuery_A function (windns.h)
description: Is the generic query interface to the DNS namespace, and provides application developers with a DNS query resolution interface. (DnsQuery_A)
helpviewer_keywords: ["DnsQuery", "DnsQuery function [DNS]", "DnsQuery_A", "_dns_dnsquery", "dns.dnsquery", "windns/DnsQuery", "windns/DnsQuery_A"]
old-location: dns\dnsquery.htm
tech.root: DNS
ms.assetid: 3d810b76-cea1-4904-9b5a-c2566b332c2c
ms.date: 12/05/2018
ms.keywords: DnsQuery, DnsQuery function [DNS], DnsQuery_A, DnsQuery_UTF8, DnsQuery_W, _dns_dnsquery, dns.dnsquery, windns/DnsQuery, windns/DnsQuery_A, windns/DnsQuery_UTF8, windns/DnsQuery_W
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DnsQuery_W (Unicode) and DnsQuery_A (ANSI)
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
 - DnsQuery_A
 - windns/DnsQuery_A
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
 - DnsQuery
 - DnsQuery_A
 - DnsQuery_W
 - DnsQuery_UTF8
---

# DnsQuery_A function


## -description

The 
<b>DnsQuery</b> function type is the generic query interface to the DNS namespace, and provides application developers with a DNS query resolution interface. Like many DNS functions, the 
<b>DnsQuery</b> function type is implemented in multiple forms to facilitate different character encoding.
		Based on the character encoding involved, use one of the following functions:
<ul>
<li><b>DnsQuery_A</b> (for ANSI encoding)</li>
<li><b>DnsQuery_W</b> (for Unicode encoding)</li>
<li><b>DnsQuery_UTF8</b> (for UTF-8 encoding)</li>
</ul>Windows 8: The <a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a> function should be used if an application requires asynchronous queries to the DNS namespace.

## -parameters

### -param pszName [in]

A pointer to a string that represents the DNS name to query.

### -param wType [in]

A value that represents the Resource Record (RR)<a href="/windows/desktop/DNS/dns-constants">DNS Record Type</a> that is queried. <b>wType</b> determines the format of data pointed to by <b>ppQueryResultsSet</b>. For example, if the value of <b>wType</b> is <b>DNS_TYPE_A</b>, the format of data pointed to by <b>ppQueryResultsSet</b> is <a href="/windows/win32/api/windns/nf-windns-dnsquery_a">DNS_A_DATA</a>.

### -param Options [in]

A value that contains a bitmap of <a href="/windows/desktop/DNS/dns-constants">DNS Query  Options</a> to use in the DNS query. Options can be combined and all options override <b>DNS_QUERY_STANDARD</b>.

### -param pExtra [in, out, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.

### -param ppQueryResults [out, optional]

Optional. A pointer to a pointer that points to the list of RRs that comprise the response. For more information, see the Remarks section.

### -param pReserved [out, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.

## -returns

Returns success confirmation upon successful completion. Otherwise, returns the appropriate DNS-specific error code as defined in Winerror.h.

## -remarks

Applications that call the 
<b>DnsQuery</b> function build a query using a fully qualified DNS name and Resource Record (RR) type, and set query options depending on the type of service desired. When the <b>DNS_QUERY_STANDARD</b> option is set, DNS uses the resolver cache, queries first with UDP, then retries with TCP if the response is truncated, and requests that the server to perform recursive resolution on behalf of the client to resolve the query.

Applications must free returned RR sets with the <a href="/windows/desktop/api/windns/nf-windns-dnsrecordlistfree">DnsRecordListFree</a> function.

<div class="alert"><b>Note</b>  When calling one of the 
<b>DnsQuery</b> function types, be aware that a DNS server may return multiple records in response to a query. A computer that is multihomed, for example, will receive multiple A records for the same IP address. The caller must use as many of the returned records as necessary.</div>
<div> </div>
Consider the following scenario, in which multiple returned records require additional activity on behalf of the application: A <b>DnsQuery_A</b> function call is made for a multihomed computer and the application finds that the address associated with the first A record is not responding. The application should then attempt to use other IP addresses specified in the (additional) A records returned from the <b>DnsQuery_A</b> function call.

 If the <i>lpstrName </i> parameter is set to <b>NULL</b>, the <b>DnsQuery</b> function fails with the error <b>INVALID_PARAMETER</b>.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsqueryex">DnsQueryEx</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsrecordlistfree">DnsRecordListFree</a>
