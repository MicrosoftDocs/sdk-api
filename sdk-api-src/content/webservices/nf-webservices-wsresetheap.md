---
UID: NF:webservices.WsResetHeap
title: WsResetHeap function (webservices.h)
description: Releases all Heap allocations. Allocations made on the Heap using WsAlloc are no longer valid. Allocation for the Heap object itself is not released.
helpviewer_keywords: ["WsResetHeap","WsResetHeap function [Web Services for Windows]","webservices/WsResetHeap","wsw.wsresetheap"]
old-location: wsw\wsresetheap.htm
tech.root: wsw
ms.assetid: c927ccb9-66c8-4acf-bbb5-12313ea80ee0
ms.date: 12/05/2018
ms.keywords: WsResetHeap, WsResetHeap function [Web Services for Windows], webservices/WsResetHeap, wsw.wsresetheap
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
 - WsResetHeap
 - webservices/WsResetHeap
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
 - WsResetHeap
---

# WsResetHeap function


## -description

Releases all Heap allocations.  Allocations made on the Heap
                using <a href="/windows/desktop/api/webservices/nf-webservices-wsalloc">WsAlloc</a> are no longer valid.  Allocation for the Heap object itself is not released.

## -parameters

### -param heap [in]

A pointer to a Heap instance to reset.
                    If the heap is not required for the given type this
                    parameter can be <b>NULL</b>.
                

The heap object.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The heap object can retain allocated memory even though it has been reset.  The amount of memory retained
                can be specified using the <a href="/windows/desktop/api/webservices/ne-webservices-ws_heap_property_id">WS_HEAP_PROPERTY_TRIM_SIZE</a> 
                property when creating the heap.