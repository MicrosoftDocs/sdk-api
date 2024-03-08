---
UID: NF:windns.DnsQueryRawResultFree
title: DnsQueryRawResultFree
description: Frees the memory allocated to a DNS_QUERY_RAW_RESULT structure object.
tech.root: DNS
ms.date: 07/13/2023
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
 - DnsQueryRawResultFree
f1_keywords:
 - DnsQueryRawResultFree
 - windns/DnsQueryRawResultFree
dev_langs:
 - c++
helpviewer_keywords:
 - DnsQueryRawResultFree
---

## -description

Frees the memory allocated to a [DNS_QUERY_RAW_RESULT](./ns-windns-dns_query_raw_result.md) structure object. Also see [DNS_QUERY_RAW_COMPLETION_ROUTINE](./nc-windns-dns_query_raw_completion_routine.md).

## -parameters

### -param queryResults

Type: \_In\_ **[DNS_QUERY_RAW_RESULT](./ns-windns-dns_query_raw_result.md)\***

The object whose memory should be freed.

## -remarks

## -see-also
