---
UID: NS:http._HTTP_REQUEST_TIMING_INFO
title: HTTP_REQUEST_TIMING_INFO
description: Contains information about how much time was spent at each request processing stage.
tech.root: http
ms.date: 01/11/2024
req.construct-type: structure
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: HTTP_REQUEST_TIMING_INFO, *PHTTP_REQUEST_TIMING_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_REQUEST_TIMING_INFO
 - http/_HTTP_REQUEST_TIMING_INFO
 - PHTTP_REQUEST_TIMING_INFO
 - http/PHTTP_REQUEST_TIMING_INFO
 - HTTP_REQUEST_TIMING_INFO
 - http/HTTP_REQUEST_TIMING_INFO
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - http.h
api_name:
 - _HTTP_REQUEST_TIMING_INFO
 - PHTTP_REQUEST_TIMING_INFO
 - HTTP_REQUEST_TIMING_INFO
helpviewer_keywords:
 - _HTTP_REQUEST_TIMING_INFO
---

## -description

Contains information about how much time was spent at each request processing stage.

## -struct-fields

### -field RequestTimingCount

Type: **[ULONG](/windows/desktop/winprog/windows-data-types)**

### -field RequestTiming[HttpRequestTimingTypeMax]

Type: **[ULONGLONG](/windows/desktop/winprog/windows-data-types)\[HttpRequestTimingTypeMax\]**

The timing types are defined in [HTTP_REQUEST_TIMING_TYPE](/windows/win32/api/http/ne-http-http_request_timing_type).

## -remarks

## -see-also
