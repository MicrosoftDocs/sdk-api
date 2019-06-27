---
UID: NF:windns.DnsStopMulticastQuery
title: DnsStopMulticastQuery function
description: Used to stop a running [DnsStartMulticastQuery](nf-windns-dnsstartmulticastquery.md) operation.
ms.date: 02/14/2019
ms.keywords: DnsStopMulticastQuery
ms.topic: language-reference
f1_keywords: 
 - "windns/DnsStopMulticastQuery"
targetos: Windows
product: Windows
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
topic_type:
 - apiref
api_type:
 - 
api_location:
 - windns.h
api_name:
 - DnsStopMulticastQuery
ms.custom: 19H1
---

## -description
Used to stop a running [DnsStartMulticastQuery](nf-windns-dnsstartmulticastquery.md) operation.

## -parameters

### -param pHandle
A pointer to the [MDNS_QUERY_HANDLE](ns-windns-mdns_query_handle.md) structure that was passed to the [DnsStartMulticastQuery](nf-windns-dnsstartmulticastquery.md) call that is to be stopped.

## -returns
If successful, returns **ERROR_SUCCESS**; otherwise, returns the appropriate DNS-specific error code as defined in `Winerror.h`. For extended error information, call [GetLastError](https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

## -see-also
