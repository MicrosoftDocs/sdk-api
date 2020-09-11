---
UID: NS:winhttp._WINHTTP_REQUEST_STATS
title: WINHTTP_REQUEST_STATS (winhttp.h)
description: The WINHTTP_REQUEST_STATS structure contains a variety of statistics for a request.
helpviewer_keywords: ["*PWINHTTP_REQUEST_STATS","WINHTTP_REQUEST_STATS","WINHTTP_REQUEST_STATS structure [HTTP]","http.winhttp_request_stats","winhttp/WINHTTP_REQUEST_STATS","WINHTTP_OPTION_REQUEST_STATS"]
old-location: 
tech.root: http
ms.assetid: 7c65777e-24eb-4713-a7b8-7263a217e8ba
ms.date: 02/25/2020
ms.keywords: '*PWINHTTP_REQUEST_STATS, WINHTTP_REQUEST_STATS, WINHTTP_REQUEST_STATS structure [HTTP], http.winhttp_request_stats, winhttp/WINHTTP_REQUEST_STATS, WINHTTP_OPTION_REQUEST_STATS'
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1903 [desktop apps only]
req.target-min-winversvr: Windows Server 2019 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WINHTTP_REQUEST_STATS, *PWINHTTP_REQUEST_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINHTTP_REQUEST_STATS
 - winhttp/_WINHTTP_REQUEST_STATS
 - PWINHTTP_REQUEST_STATS
 - winhttp/PWINHTTP_REQUEST_STATS
 - WINHTTP_REQUEST_STATS
 - winhttp/WINHTTP_REQUEST_STATS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winhttp.h
api_name:
 - WINHTTP_REQUEST_STATS
---

## -description

The **WINHTTP\_REQUEST\_STATS** structure contains a variety of statistics for a request.

## -struct-fields

### -field ullFlags

Flags containing details on how the request was made. The following flags are available.

| Value | Meaning |
|-|-|
| WINHTTP_REQUEST_STAT_FLAG_TCP_FAST_OPEN | TCP Fast Open occurred. |
| WINHTTP_REQUEST_STAT_FLAG_TLS_SESSION_RESUMPTION | TLS Session Resumption occurred. |
| WINHTTP_REQUEST_STAT_FLAG_TLS_FALSE_START | TLS False Start occurred. |
| WINHTTP_REQUEST_STAT_FLAG_PROXY_TLS_SESSION_RESUMPTION | TLS Session Resumption occurred for the proxy connection. |
| WINHTTP_REQUEST_STAT_FLAG_PROXY_TLS_FALSE_START | TLS False Start occurred for the proxy connection. |
| WINHTTP_REQUEST_STAT_FLAG_FIRST_REQUEST | This is the first request on the connection. |

### -field ulIndex

The index of the request on the connection. This indicates how many prior requests were sent over the shared connection.

### -field cStats

Unsigned long integer value that contains the number of statistics to retrieve. This should generally be set to **WinHttpRequestStatLast**.

### -field rgullStats

Array of unsigned long long integer values that will contain the returned statistics, indexed by [**WINHTTP\_REQUEST\_STAT\_ENTRY**](/windows/desktop/api/winhttp/ne-winhttp-winhttp_request_stat_entry).

## -remarks

This structure is used with [WinHttpQueryOption](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption) to retrieve statistics for a request by specifying the **WINHTTP\_OPTION\_REQUEST\_STATS** flag.

## -see-also

[WinHttpQueryOption](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption)

