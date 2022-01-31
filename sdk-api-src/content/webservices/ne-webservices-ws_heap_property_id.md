---
UID: NE:webservices.__unnamed_enum_34
title: WS_HEAP_PROPERTY_ID (webservices.h)
description: Each heap property is identified by an ID and has an associated value.
helpviewer_keywords: ["WS_HEAP_PROPERTY_ACTUAL_SIZE","WS_HEAP_PROPERTY_ID","WS_HEAP_PROPERTY_ID enumeration [Web Services for Windows]","WS_HEAP_PROPERTY_MAX_SIZE","WS_HEAP_PROPERTY_REQUESTED_SIZE","WS_HEAP_PROPERTY_TRIM_SIZE","webservices/WS_HEAP_PROPERTY_ACTUAL_SIZE","webservices/WS_HEAP_PROPERTY_ID","webservices/WS_HEAP_PROPERTY_MAX_SIZE","webservices/WS_HEAP_PROPERTY_REQUESTED_SIZE","webservices/WS_HEAP_PROPERTY_TRIM_SIZE","wsw.ws_heap_property_id"]
old-location: wsw\ws_heap_property_id.htm
tech.root: wsw
ms.assetid: c047a3b9-27a1-464c-b9f9-0b0c6cf8eb97
ms.date: 12/05/2018
ms.keywords: WS_HEAP_PROPERTY_ACTUAL_SIZE, WS_HEAP_PROPERTY_ID, WS_HEAP_PROPERTY_ID enumeration [Web Services for Windows], WS_HEAP_PROPERTY_MAX_SIZE, WS_HEAP_PROPERTY_REQUESTED_SIZE, WS_HEAP_PROPERTY_TRIM_SIZE, webservices/WS_HEAP_PROPERTY_ACTUAL_SIZE, webservices/WS_HEAP_PROPERTY_ID, webservices/WS_HEAP_PROPERTY_MAX_SIZE, webservices/WS_HEAP_PROPERTY_REQUESTED_SIZE, webservices/WS_HEAP_PROPERTY_TRIM_SIZE, wsw.ws_heap_property_id
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WS_HEAP_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_HEAP_PROPERTY_ID
 - webservices/WS_HEAP_PROPERTY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_HEAP_PROPERTY_ID
---

# WS_HEAP_PROPERTY_ID enumeration


## -description

Each heap property is identified by an ID and has an associated value.

## -enum-fields

### -field WS_HEAP_PROPERTY_MAX_SIZE:0

Used with <a href="/windows/desktop/api/webservices/nf-webservices-wsgetheapproperty">WsGetHeapProperty</a>.  Returns
                    the total number of bytes that can be allocated from the heap.  The total
                    number of bytes is defined as sum of the sizes passed in all the calls to
                    <a href="/windows/desktop/api/webservices/nf-webservices-wsalloc">WsAlloc</a> since the heap was created / reset.

### -field WS_HEAP_PROPERTY_TRIM_SIZE:1

Used with <a href="/windows/desktop/api/webservices/nf-webservices-wsgetheapproperty">WsGetHeapProperty</a>.  
                    Returns the maximum number of bytes of memory that the heap will
                    retain after a call to <a href="/windows/desktop/api/webservices/nf-webservices-wsresetheap">WsResetHeap</a> call.  This should 
                    be treated an approximate value due to heap overhead.  If the
                    trim size is larger than the max size, then the size of the
                    heap will not be trimmed.

### -field WS_HEAP_PROPERTY_REQUESTED_SIZE:2

Used with <a href="/windows/desktop/api/webservices/nf-webservices-wsgetheapproperty">WsGetHeapProperty</a>.  Returns the current 
                    total number of bytes requested from the heap since the heap was 
                    created/reset.

### -field WS_HEAP_PROPERTY_ACTUAL_SIZE:3

Used with <a href="/windows/desktop/api/webservices/nf-webservices-wsgetheapproperty">WsGetHeapProperty</a>.  Returns the current
                    total number of bytes that the WS_HEAP has allocated from the
                    operating system for purposes of providing allocations.
