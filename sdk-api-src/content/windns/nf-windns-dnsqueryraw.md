---
UID: NF:windns.DnsQueryRaw
title: DnsQueryRaw
description: Enables you to perform a DNS query that accepts either a raw packet containing a DNS query, or a query name and type.
tech.root: DNS
ms.date: 07/11/2023
targetos: Windows
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: dnsapi.dll
req.header: windns.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: dnsapi.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dnsapi.dll
api_name:
 - DnsQueryRaw
f1_keywords:
 - DnsQueryRaw
 - windns/DnsQueryRaw
dev_langs:
 - c++
helpviewer_keywords:
 - DnsQueryRaw
---

## -description

Enables you to perform a DNS query that accepts either a raw packet containing a DNS query, or a query name and type. You can augment the query with settings and configuration from the host system.

* You can apply new query options and custom servers to an already-formatted raw DNS query packet.
* Or you can instead provide a query name and type, and receive both the parsed records and raw result packet (allowing clients to interact with all information received from the server).

Queries are performed asynchronously; and results are passed to a [DNS_QUERY_RAW_COMPLETION_ROUTINE](nc-windns-dns_query_raw_completion_routine.md) asynchronous callback function that you implement. To cancel a query, call [DnsCancelQueryRaw](./nf-windns-dnscancelqueryraw.md).

## -parameters

### -param queryRequest

Type: \_In\_ **[DNS_QUERY_RAW_REQUEST](./ns-windns-dns_query_raw_request.md)\***

The query request.

### -param cancelHandle

Type: \_Inout\_ **[DNS_QUERY_RAW_CANCEL](./ns-windns-dns_query_raw_cancel.md)\***

Used to obtain a cancel handle, which you can pass to [DnsCancelQueryRaw](./nf-windns-dnscancelqueryraw.md) should you need to cancel the query.

## -returns

A **DNS_STATUS** value indicating success or failure. If **DNS_REQUEST_PENDING** is returned, then when the query completes, the system calls the [DNS_QUERY_RAW_COMPLETION_ROUTINE](nc-windns-dns_query_raw_completion_routine.md) implementation that you passed in the *queryCompletionCallback* member of *queryRequest*. That callback will received the results of the query if successful, or any failures or cancellations.

## -remarks

The structure of a raw packet is the wire representation of the DNS query and response as documented by RFC 1035. A 12-byte DNS header is followed by either a question section for the query, or by a variable number (can be 0) of records for the response. If TCP is used, then the raw packet must be prefixed with a 2-byte *length* field. That can be used to apply host NRPT rules, or to perform encrypted DNS queries, among other things.

## -see-also
