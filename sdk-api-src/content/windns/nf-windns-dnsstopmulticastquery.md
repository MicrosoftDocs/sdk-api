---
UID: NF:windns.DnsStopMulticastQuery
title: DnsStopMulticastQuery function
description: Used to stop a running [DnsStartMulticastQuery](../windns/nf-windns-dnsstartmulticastquery.md) operation.
tech.root: dns
helpviewer_keywords: ["DnsStopMulticastQuery"]
ms.date: 02/14/2019
ms.keywords: DnsStopMulticastQuery
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
 - DnsStopMulticastQuery
 - windns/DnsStopMulticastQuery
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - windns.h
api_name:
 - DnsStopMulticastQuery
---

## -description

Used to stop a running [DnsStartMulticastQuery](/windows/win32/api/windns/nf-windns-dnsstartmulticastquery) operation.

## -parameters

### -param pHandle

A pointer to the [MDNS_QUERY_HANDLE](ns-windns-mdns_query_handle.md) structure that was passed to the [DnsStartMulticastQuery](nf-windns-dnsstartmulticastquery.md) call that is to be stopped.

## -returns

If successful, returns **ERROR_SUCCESS**; otherwise, returns the appropriate DNS-specific error code as defined in `Winerror.h`. For extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

## -see-also