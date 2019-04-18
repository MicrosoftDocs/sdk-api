---
UID: NC:windns.MDNS_QUERY_CALLBACK
title: MDNS_QUERY_CALLBACK callback function
description: Used to asynchronously return the results of an mDNS query.
ms.date: 02/19/2019
ms.keywords: MDNS_QUERY_CALLBACK
ms.topic: language-reference
targetos: Windows
product: Windows
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
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.typenames: MDNS_QUERY_CALLBACK
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - windns.h
api_name:
 - MDNS_QUERY_CALLBACK
ms.custom: 19H1
---

## -description
Used to asynchronously return the results of an mDNS query.

## -parameters

    _In_    PVOID pQueryContext,
    _Inout_ PMDNS_QUERY_HANDLE pQueryHandle,
    _Inout_ PDNS_QUERY_RESULT pQueryResults

### -param pQueryContext
A pointer to the user context that was passed to [DnsServiceBrowse](nf-windns-dnsservicebrowse.md).

### -param pQueryHandle
A pointer to the [MDNS_QUERY_HANDLE](ns-windns-mdns_query_handle.md) structure that was passed to [DnsStartMulticastQuery](nf-windns-dnsstartmulticastquery.md).

### -param pQueryResults
A pointer to a [DNS_QUERY_RESULT](/windows/desktop/api/windns/ns-windns-_dns_query_result) structure that contains the query results. Your application is responsible for freeing the `pQueryRecords` contained in this structure using [DnsRecordListFree](/windows/desktop/api/windns/nf-windns-dnsrecordlistfree).

## -returns
This callback function does not return a value.

## -remarks

## -see-also
