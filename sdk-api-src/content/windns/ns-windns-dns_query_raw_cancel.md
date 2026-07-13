---
UID: NS:windns._DNS_QUERY_RAW_CANCEL
title: DNS_QUERY_RAW_CANCEL
description: Represents a DNS raw query cancel handle.
tech.root: DNS
ms.date: 07/17/2023
targetos: Windows
prerelease: true
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: windns.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.typenames: DNS_QUERY_RAW_CANCEL
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - _DNS_QUERY_RAW_CANCEL
 - DNS_QUERY_RAW_CANCEL
f1_keywords:
 - _DNS_QUERY_RAW_CANCEL
 - windns/_DNS_QUERY_RAW_CANCEL
 - DNS_QUERY_RAW_CANCEL
 - windns/DNS_QUERY_RAW_CANCEL
dev_langs:
 - c++
helpviewer_keywords:
 - _DNS_QUERY_RAW_CANCEL
---

## -description

Represents a DNS raw query cancel handle (see [DnsQueryRaw](./nf-windns-dnsqueryraw.md) and [DnsCancelQueryRaw](./nf-windns-dnscancelqueryraw.md)).

This structure must persist until the query completion callback is made (see [DNS_QUERY_RAW_COMPLETION_ROUTINE](nc-windns-dns_query_raw_completion_routine.md)), and it can't be copied elsewhere after it's been passed into [DnsQueryRaw](./nf-windns-dnsqueryraw.md). If the query completion callback hasn't been called by the time [DnsCancelQueryRaw](./nf-windns-dnscancelqueryraw.md) returns, then the query completion callback will lead to the callback being made with a *queryStatus* of **ERROR_CANCELLED** in the *queryResults* parameter. No special cleanup is required for this structure once the query is complete. Similar to the cancel structure used for [DnsQueryEx](./nf-windns-dnsqueryex.md); for more details, see [DNS_QUERY_CANCEL](./ns-windns-dns_query_cancel.md).

## -struct-fields

### -field reserved

Type: **[CHAR](/windows/win32/winprog/windows-data-types)\[\]**

Opaque handle structure used for cancel.

## -remarks

## -see-also
