---
UID: NF:windns.DnsQueryEx
title: DnsQueryEx function (windns.h)
description: The asynchronous generic query interface to the DNS namespace, and provides application developers with a DNS query resolution interface.
helpviewer_keywords: ["DnsQueryEx","DnsQueryEx function [DNS]","dns.dnsqueryex","windns/DnsQueryEx"]
old-location: dns\dnsqueryex.htm
tech.root: DNS
ms.assetid: 22664B9A-5010-42E7-880B-8D5B16A9F2DC
ms.date: 12/05/2018
ms.keywords: DnsQueryEx, DnsQueryEx function [DNS], dns.dnsqueryex, windns/DnsQueryEx
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
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsQueryEx
 - windns/DnsQueryEx
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
 - DnsQueryEx
---

## -description

The <b>DnsQueryEx</b> function is the asynchronous generic query interface to the DNS namespace. It provides application developers with a DNS query resolution interface.

Like <a href="/windows/win32/api/windns/nf-windns-dnsquery_a">DnsQuery</a>, <b>DnsQueryEx</b> can be used to make synchronous queries to the DNS namespace as well.

## -parameters

### -param pQueryRequest [in]

A pointer to a <a href="/windows/win32/api/windns/ns-windns-dns_query_request">DNS_QUERY_REQUEST</a> or <a href="/windows/win32/api/windns/ns-windns-dns_query_request3">DNS_QUERY_REQUEST3</a> structure that contains the query request information.

<div class="alert"><b>Note</b>  By omitting the <a href="/windows/win32/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> callback from the <b>pQueryCompleteCallback</b> member of this structure, <b>DnsQueryEx</b> is called synchronously.</div>
<div> </div>

### -param pQueryResults [in, out]

A pointer to a <a href="/windows/win32/api/windns/ns-windns-dns_query_result">DNS_QUERY_RESULT</a> structure that contains the results of the query. On input, the <b>version</b> member of  <i>pQueryResults</i> must be <b>DNS_QUERY_RESULTS_VERSION1</b> and all other members should be <b>NULL</b>. On output, the remaining members will be filled as part of the query complete. 

<div class="alert"><b>Note</b>  For asynchronous queries, an application should not free
                            this structure until the <a href="/windows/win32/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> callback is invoked. When the query completes, the <a href="/windows/win32/api/windns/ns-windns-dns_query_result">DNS_QUERY_RESULT</a> structure contains a pointer to a list of
                            <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORDS</a> that should be freed using <a href="/windows/win32/api/windns/nf-windns-dnsrecordlistfree">DnsRecordListFree</a>.</div>
<div> </div>

### -param pCancelHandle [in, out, optional]

A pointer to a <a href="/windows/win32/api/windns/ns-windns-dns_query_cancel">DNS_QUERY_CANCEL</a> structure that can be used to cancel a
                            pending asynchronous query.

<div class="alert"><b>Note</b>  An application should not free
                            this structure until the <a href="/windows/win32/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> callback is invoked.</div>
<div> </div>

## -returns

The 
<b>DnsQueryEx</b> function has the following possible return values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The call was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Either the <i>pQueryRequest</i> or <i>pQueryResults</i> parameters are uninitialized or contain the wrong version. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DNS RCODE</b></dt>
</dl>
</td>
<td width="60%">
The call resulted in an <a href="/windows/desktop/DNS/dns-constants">RCODE</a> error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DNS_INFO_NO_RECORDS</b></dt>
</dl>
</td>
<td width="60%">
No records in the response.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DNS_REQUEST_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The query will be completed asynchronously.

</td>
</tr>
</table>

## -remarks

If a call to <b>DnsQueryEx</b> completes synchronously (i.e., the function return value is not <b>DNS_REQUEST_PENDING</b>), the <b>pQueryRecords</b> member of <i>pQueryResults</i> contains a pointer to a list of <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORDS</a> and <b>DnsQueryEx</b> will return either error or success.

The following conditions invoke a synchronous call to <b>DnsQueryEx</b> and do not utilize the DNS callback:

<ul>
<li>The <a href="/windows/win32/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> callback is omitted from the <b>pQueryCompleteCallback</b> member of <i>pQueryRequest</i>.</li>
<li>A query is for the local machine name and <a href="/windows/win32/api/windns/nf-windns-dnsquery_a">A</a> or <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_aaaa_data">AAAA</a> type Resource Records (RR).</li>
<li>A call to <b>DnsQueryEx</b> queries an IPv4 or IPv6 address.</li>
<li>A call to <b>DnsQueryEx</b> returns in error.</li>
</ul>
If a call to <b>DnsQueryEx</b> completes asynchronously, the results of the query are returned by the <a href="/windows/win32/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> callback in <i>pQueryRequest</i>, the <b>QueryStatus</b> member of <i>pQueryResults</i> contains <b>DNS_REQUEST_PENDING</b>, and <b>DnsQueryEx</b> returns <b>DNS_REQUEST_PENDING</b>. Applications should track the <i>pQueryResults</i> structure that is passed into <b>DnsQueryEx</b> until the DNS callback succeeds. Applications can cancel an asynchronous query using the <i>pCancelHandle</i> handle returned by <b>DnsQueryEx</b>.

<i>pCancelHandle</i> returned from an asynchronous call to <b>DnsQueryEx</b> and <i>pQueryContext</i> is valid until the <a href="/windows/win32/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> DNS callback is invoked.

<div class="alert"><b>Note</b>  Applications are notified of asynchronous <b>DnsQueryEx</b> completion through the <a href="/windows/win32/api/windns/nc-windns-dns_query_completion_routine">DNS_QUERY_COMPLETION_ROUTINE</a> callback within the same process context.</div>
<div> </div>

## -see-also

* [DNS_QUERY_COMPLETION_ROUTINE](/windows/win32/api/windns/nc-windns-dns_query_completion_routine)
* [DnsCancelQuery](/windows/win32/api/windns/nf-windns-dnscancelquery)
* [DnsQuery](/windows/win32/api/windns/nf-windns-dnsquery_a)
