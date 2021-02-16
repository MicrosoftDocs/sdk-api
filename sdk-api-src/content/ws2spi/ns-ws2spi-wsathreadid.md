---
UID: NS:ws2spi._WSATHREADID
title: WSATHREADID
description: The WSATHREADID structure enables a provider to identify a thread on which asynchronous procedure calls (APCs) can be queued using the WPUQueueApc function.
tech.root: winsock
helpviewer_keywords: ["_WSATHREADID","WSATHREADID"]
ms.date: 4/26/2019
ms.keywords: _WSATHREADID, WSATHREADID
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ws2spi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.target-type: 
req.typenames: WSATHREADID, *LPWSATHREADID
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ws2spi.h
api_name:
 - _WSATHREADID
 - WSATHREADID
f1_keywords:
 - _WSATHREADID
 - ws2spi/_WSATHREADID
 - LPWSATHREADID
 - ws2spi/LPWSATHREADID
 - WSATHREADID
 - ws2spi/WSATHREADID
---

## -description

The **WSATHREADID** structure enables a provider to identify a thread on which asynchronous procedure calls (APCs) can be queued using the [**WPUQueueApc**](./nf-ws2spi-wpuqueueapc.md) function.

## -struct-fields

```C++
} WSATHREADID, *LPWSATHREADID;
```

### -field ThreadHandle

Handle to the thread ID.

### -field Reserved

Reserved.

## -remarks

## -see-also

<b><a href="/windows/win32/api/ws2spi/nf-ws2spi-wpuqueueapc">WPUQueueApc</a></b>
   
<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspioctl">LPWSPIoctl</a></b>   

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwsprecv">LPWSPRecv</a></b>
   

<b><a href="/windows/win32/api/ws2spi/nc-ws2spi-lpwspsend">LPWSPSend</a></b>