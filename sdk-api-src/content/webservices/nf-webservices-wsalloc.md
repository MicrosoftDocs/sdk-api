---
UID: NF:webservices.WsAlloc
title: WsAlloc function (webservices.h)
description: Allocates a segment of memory from the specified heap.
helpviewer_keywords: ["WsAlloc","WsAlloc function [Web Services for Windows]","webservices/WsAlloc","wsw.wsalloc"]
old-location: wsw\wsalloc.htm
tech.root: wsw
ms.assetid: 633b6a11-09ba-48a7-a1ad-940846c65d79
ms.date: 12/05/2018
ms.keywords: WsAlloc, WsAlloc function [Web Services for Windows], webservices/WsAlloc, wsw.wsalloc
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsAlloc
 - webservices/WsAlloc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsAlloc
---

# WsAlloc function


## -description

Allocates a segment of memory from the specified <a href="/windows/desktop/wsw/heap">heap</a>.

## -parameters

### -param heap [in]

Pointer to a <a href="/windows/desktop/wsw/ws-heap">WS_HEAP</a> structure representing the heap from which to allocate the memory.

### -param size [in]

The number of bytes to allocate.  This value can be zero.

### -param ptr

On success, a pointer that receives the address of the allocated memory. This pointer is valid until <a href="/windows/desktop/api/webservices/nf-webservices-wsfreeheap">WsFreeHeap</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsresetheap">WsResetHeap</a> is called on the <a href="/windows/desktop/wsw/heap">heap</a>. 



The returned pointer is aligned on an 8-byte boundary. 



Zero byte allocations will return a non-NULL pointer.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The requested bytes, in addition to already allocated bytes, exceed the size of the <a href="/windows/desktop/wsw/heap">heap</a>, as specified by the <a href="/windows/desktop/api/webservices/ne-webservices-ws_heap_property_id">WS_HEAP_PROPERTY_MAX_SIZE</a> property.  
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

The memory returned by this function is not zero initialized and contains undefined values.