---
UID: NF:windns.DnsCancelQueryRaw
title: DnsCancelQueryRaw
description: Cancels a query that was initiated by calling DnsQueryRaw.
tech.root: DNS
ms.date: 07/17/2023
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
 - DnsCancelQueryRaw
f1_keywords:
 - DnsCancelQueryRaw
 - windns/DnsCancelQueryRaw
dev_langs:
 - c++
helpviewer_keywords:
 - DnsCancelQueryRaw
---

## -description

Cancels a query that was initiated by calling [DnsQueryRaw](./nf-windns-dnsqueryraw.md).

If the query completion callback (see [DNS_QUERY_RAW_COMPLETION_ROUTINE](nc-windns-dns_query_raw_completion_routine.md)) hasn't been called by the time **DnsCancelQueryRaw** returns, then the query completion callback will lead to the callback being made with a *queryStatus* of **ERROR_CANCELLED** in the *queryResults* parameter.

## -parameters

### -param cancelHandle

Type: \_In\_ **[DNS_QUERY_RAW_CANCEL](./ns-windns-dns_query_raw_cancel.md)\***

The cancel handle that you obtained by calling [DnsQueryRaw](./nf-windns-dnsqueryraw.md). 

## -returns

A **DNS_STATUS** value indicating success or failure.

## -remarks

## -see-also
