---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# WS_HEAP_PROPERTY_ID enumeration


## -description



                Each heap property is identified by an ID and has an associated value.
            


## -enum-fields




### -field WS_HEAP_PROPERTY_MAX_SIZE


                    Used with <a href="https://msdn.microsoft.com/c463924a-1491-4d65-86ed-827327e560b9">WsGetHeapProperty</a>.  Returns
                    the total number of bytes that can be allocated from the heap.  The total
                    number of bytes is defined as sum of the sizes passed in all the calls to
                    <a href="https://msdn.microsoft.com/633b6a11-09ba-48a7-a1ad-940846c65d79">WsAlloc</a> since the heap was created / reset.
                


### -field WS_HEAP_PROPERTY_TRIM_SIZE


                    Used with <a href="https://msdn.microsoft.com/c463924a-1491-4d65-86ed-827327e560b9">WsGetHeapProperty</a>.  
                    Returns the maximum number of bytes of memory that the heap will
                    retain after a call to <a href="https://msdn.microsoft.com/c927ccb9-66c8-4acf-bbb5-12313ea80ee0">WsResetHeap</a> call.  This should 
                    be treated an approximate value due to heap overhead.  If the
                    trim size is larger than the max size, then the size of the
                    heap will not be trimmed.
                


### -field WS_HEAP_PROPERTY_REQUESTED_SIZE


                    Used with <a href="https://msdn.microsoft.com/c463924a-1491-4d65-86ed-827327e560b9">WsGetHeapProperty</a>.  Returns the current 
                    total number of bytes requested from the heap since the heap was 
                    created/reset.
                


### -field WS_HEAP_PROPERTY_ACTUAL_SIZE


                    Used with <a href="https://msdn.microsoft.com/c463924a-1491-4d65-86ed-827327e560b9">WsGetHeapProperty</a>.  Returns the current
                    total number of bytes that the WS_HEAP has allocated from the
                    operating system for purposes of providing allocations.
                

