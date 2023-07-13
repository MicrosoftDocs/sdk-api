---
UID: NC:windns.DNS_QUERY_RAW_COMPLETION_ROUTINE
title: DNS_QUERY_RAW_COMPLETION_ROUTINE
description: The function signature of an asynchronous callback function that you implement. The system calls your implementation with the results of a query that you initiated by calling DnsQueryRaw.
tech.root: DNS
ms.date: 07/13/2023
targetos: Windows
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: windns.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - windns.h
api_name:
 - DNS_QUERY_RAW_COMPLETION_ROUTINE
f1_keywords:
 - DNS_QUERY_RAW_COMPLETION_ROUTINE
 - windns/DNS_QUERY_RAW_COMPLETION_ROUTINE
dev_langs:
 - c++
helpviewer_keywords:
 - DNS_QUERY_RAW_COMPLETION_ROUTINE
---

## -description

**DNS_QUERY_RAW_COMPLETION_ROUTINE** is the function signature of an asynchronous callback function that you implement. The system calls your implementation with the results of a query that you initiated by calling [DnsQueryRaw](./nf-windns-dnsqueryraw.md). The results contain both the parsed records and the raw result packet, to be passed on to later systems as desired. The result provides information about the server that provided the results.

The system calls this callback on query completion if **DnsQueryRaw** returns **DNS_REQUEST_PENDING**; and it will indicate the results of the query if successful, or any failures or cancellations.

## -parameters

### -param queryContext

Type: \_In\_ **[VOID](/windows/win32/winprog/windows-data-types)\***

A pointer to the query context that was passed into [DnsQueryRaw](./nf-windns-dnsqueryraw.md) through the *queryContext* field of [DNS_QUERY_RAW_REQUEST](./ns-windns-dns_query_raw_request.md).

### -param queryResults

Type: \_Inout\_ **[DNS_QUERY_RAW_RESULT](./ns-windns-dns_query_raw_result.md)\***

A pointer to the results of the query. If this callback is made because of a query cancellation through [DnsCancelQueryRaw](./nf-windns-dnscancelqueryraw.md), then the *queryStatus* field in *queryResults* will be set to **ERROR_CANCELLED**.

If it's not `NULL`, then you must free the *queryResults* pointer by using [DnsQueryRawResultFree](./nf-windns-dnsqueryrawresultfree.md).

## -remarks

## -see-also
