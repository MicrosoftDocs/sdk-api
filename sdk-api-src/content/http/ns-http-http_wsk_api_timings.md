---
UID: NS:http._HTTP_WSK_API_TIMINGS
title: HTTP_WSK_API_TIMINGS
description: Represents statistics on the time spent on specific API calls.
ms.date: 09/19/2025
tech.root: http
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: http.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: HTTP_WSK_API_TIMINGS, *PHTTP_WSK_API_TIMINGS
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - http.h
api_name:
 - _HTTP_WSK_API_TIMINGS
 - PHTTP_WSK_API_TIMINGS
 - HTTP_WSK_API_TIMINGS
f1_keywords:
 - _HTTP_WSK_API_TIMINGS
 - http/_HTTP_WSK_API_TIMINGS
 - PHTTP_WSK_API_TIMINGS
 - http/PHTTP_WSK_API_TIMINGS
 - HTTP_WSK_API_TIMINGS
 - http/HTTP_WSK_API_TIMINGS
dev_langs:
 - c++
helpviewer_keywords:
 - _HTTP_WSK_API_TIMINGS
---

## -description

Represents statistics on the time spent on specific API calls.

## -struct-fields

### -field ConnectCount

Tracks the number of times that **Connect** was called.

### -field ConnectSum

Tracks the number of ticks of the high-performance counter that have been spent in **Connect** calls for the socket.

### -field DisconnectCount

Tracks the number of times that **Disconnect** was called.

### -field DisconnectSum

Tracks the number of ticks of the high-performance counter that have been spent in **Disconnect** calls for the socket.

### -field SendCount

Tracks the number of times that **Send** was called.

### -field SendSum

Tracks the number of ticks of the high-performance counter that have been spent in **Send** calls for the socket.

### -field ReceiveCount

Tracks the number of times that **Receive** was called.

### -field ReceiveSum

Tracks the number of ticks of the high-performance counter that have been spent in **Receive** calls for the socket.

### -field ReleaseCount

Tracks the number of times that **Release** was called.

### -field ReleaseSum

Tracks the number of ticks of the high-performance counter that have been spent in **Release** calls for the socket.

### -field ControlSocketCount

Tracks the number of times that **ControlSocket** was called.

### -field ControlSocketSum

Tracks the number of ticks of the high-performance counter that have been spent in **ControlSocket** calls for the socket.

## -remarks

`Http.sys` can provide statistics on the time spent on specific API calls as listed here. Since the gathering of statistics has a slight overhead in time and memory, there's a registry key that you'll need to set in order to enable using **HTTP_WSK_API_TIMINGS**. For more details, see the notes in [HTTP_REQUEST_PROPERTY](./ne-http-http_request_property.md).

To check the actual duration of an HPC tick, see [QueryPerformanceFrequency](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).

## -see-also
