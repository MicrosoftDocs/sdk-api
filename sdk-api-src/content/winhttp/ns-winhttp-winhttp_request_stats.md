---
UID: NS:winhttp._WINHTTP_REQUEST_STATS
title: WINHTTP_REQUEST_STATS (winhttp.h)
description: The WINHTTP_REQUEST_STATS structure contains a variety of statistics for a request.
old-location:
tech.root: WinHttp
ms.assetid: 7c65777e-24eb-4713-a7b8-7263a217e8ba
ms.date: 02/25/2020
ms.keywords: '*LPWINHTTP_REQUEST_STATS, WINHTTP_REQUEST_STATS, WINHTTP_REQUEST_STATS structure [HTTP], http.winhttp_request_stats, winhttp/WINHTTP_REQUEST_STATS, WINHTTP_OPTION_REQUEST_STATS'
f1_keywords:
- winhttp/WINHTTP_REQUEST_STATS
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Winhttp.h
api_name:
- WINHTTP_REQUEST_STATS
targetos: Windows
req.typenames: WINHTTP_REQUEST_STATS, *LPWINHTTP_REQUEST_STATS
req.redist:
ms.custom: 19H1
---

# WINHTTP_REQUEST_STATS structure


## -description

The **WINHTTP\_REQUEST\_STATS** structure contains a variety of statistics for a request.


## -struct-fields


### -field cStats

Unsigned long integer value that contains the number of statistics to retrieve. This should generally be set to **WinHttpRequestStatLast**.


### -field rgullStats

Array of unsigned long long integer values that will contain the returned statistics, indexed by [**WINHTTP\_REQUEST\_STAT\_ENTRY**](/windows/desktop/api/winhttp/ne-winhttp-winhttp_request_stat_entry).


## -remarks

This structure is used with [WinHttpQueryOption](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption) to retrieve statistics for a request by specifying the **WINHTTP\_OPTION\_REQUEST\_STATS** flag.


## -see-also

[WinHttpQueryOption](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption)
