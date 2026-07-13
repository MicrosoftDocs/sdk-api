---
UID: NF:windns.DnsStartMulticastQuery
title: DnsStartMulticastQuery function
description: Used to register a discoverable service on this device. (DnsStartMulticastQuery)
tech.root: dns
helpviewer_keywords: ["DnsStartMulticastQuery"]
ms.date: 02/14/2019
ms.keywords: DnsStartMulticastQuery
targetos: Windows
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
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
f1_keywords:
 - DnsStartMulticastQuery
 - windns/DnsStartMulticastQuery
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - windns.h
api_name:
 - DnsStartMulticastQuery
---

## -description

Used to register a discoverable service on this device.

## -parameters

### -param pQueryRequest

A pointer to an [MDNS_QUERY_REQUEST](ns-windns-mdns_query_request.md) structure that contains information about the query to be performed.

### -param pHandle

A pointer to an [MDNS_QUERY_HANDLE](ns-windns-mdns_query_handle.md) structure that will be populated with the necessary data. This structure is to be passed later to [DnsStopMulticastQuery](nf-windns-dnsstopmulticastquery.md) to stop the query.

## -returns

If successful, returns **ERROR_SUCCESS**; otherwise, returns the appropriate DNS-specific error code as defined in `Winerror.h`. For extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

This function is asynchronous. The query runs indefinitely, until [DnsStopMulticastQuery](nf-windns-dnsstopmulticastquery.md) is called. For each response from the network, the query callback will be invoked with the appropriate status and results.

## -see-also
