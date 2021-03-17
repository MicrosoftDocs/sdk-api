---
UID: NS:winhttp._WINHTTP_REQUEST_TIMES
title: WINHTTP_REQUEST_TIMES (winhttp.h)
description: The WINHTTP_REQUEST_TIMES structure contains a variety of timing information for an HTTP request.
helpviewer_keywords: ["*PWINHTTP_REQUEST_TIMES","WINHTTP_REQUEST_TIMES","WINHTTP_REQUEST_TIMES structure [HTTP]","http.winhttp_request_times","winhttp/WINHTTP_REQUEST_TIMES","WINHTTP_OPTION_REQUEST_TIMES"]
old-location: 
tech.root: http
ms.assetid: 4d30cd0a-88ea-4d03-951d-be50c017efd3
ms.date: 02/25/2020
ms.keywords: '*PWINHTTP_REQUEST_TIMES, WINHTTP_REQUEST_TIMES, WINHTTP_REQUEST_TIMES structure [HTTP], http.winhttp_request_times, winhttp/WINHTTP_REQUEST_TIMES, WINHTTP_OPTION_REQUEST_TIMES'
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
req.typenames: WINHTTP_REQUEST_TIMES, *PWINHTTP_REQUEST_TIMES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINHTTP_REQUEST_TIMES
 - winhttp/_WINHTTP_REQUEST_TIMES
 - PWINHTTP_REQUEST_TIMES
 - winhttp/PWINHTTP_REQUEST_TIMES
 - WINHTTP_REQUEST_TIMES
 - winhttp/WINHTTP_REQUEST_TIMES
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
 - WINHTTP_REQUEST_TIMES
---

## -description

The **WINHTTP\_REQUEST\_TIMES** structure contains a variety of timing information for a request.

## -struct-fields

### -field cTimes

Unsigned long integer value that contains the number of timings to retrieve. This should generally be set to **WinHttpRequestTimeLast**.

### -field rgullTimes

Array of unsigned long long integer values that will contain the returned timings, indexed by [**WINHTTP\_REQUEST\_TIME\_ENTRY**](/windows/desktop/api/winhttp/ne-winhttp-winhttp_request_time_entry).

Times are measured as performance counter values; for more information, see [QueryPerformanceCounter](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter).

## -remarks

This structure is used with [WinHttpQueryOption](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption) to retrieve timing information for a request by specifying the **WINHTTP\_OPTION\_REQUEST\_TIMES** flag.

## -see-also

[WinHttpQueryOption](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption)

[QueryPerformanceCounter](/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter)

