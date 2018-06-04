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

# WsCreateHeap function


## -description



Creates a <a href="https://msdn.microsoft.com/library/windows/hardware/dn926854">heap</a> object.
            




## -parameters




### -param maxSize [in]

The total number of bytes that can be allocated from the heap.  The total
                  number of bytes is defined as sum of the sizes passed in all the calls to
                                    the <a href="https://msdn.microsoft.com/633b6a11-09ba-48a7-a1ad-940846c65d79">WsAlloc</a> function since the heap was created or reset.


### -param trimSize [in]

The maximum number of bytes of memory that the heap
                retains after the heap has been reset by a call to the  <a href="https://msdn.microsoft.com/c927ccb9-66c8-4acf-bbb5-12313ea80ee0">WsResetHeap</a> function.  This is an approximation value due to heap overhead.  <div class="alert"><b>Note</b>  If the
                value of <i>trimSize</i> is larger than the value of  <i>maxSize</i>,  the size of the
                heap will not be adjusted to the desired size.</div>
<div> </div>



### -param properties [in, optional]

                    Reserved for future use; set to <b>NULL</b>.



### -param propertyCount [in]


                    Reserved for future use; set to 0 (zero). 
                


### -param heap


                    On   success, pointer that receives the address of the  <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> structure representing the new heap object.
                


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.




## -remarks



A heap in Windows Web Services API  is a memory allocation used for <a href="https://msdn.microsoft.com/edc810d9-7d78-4b79-8cbb-e87401f6ae41">messages</a>.  Heaps can also be used to store message data separately from the lifetime of a message. Some API functions allow for  explicit heap control over the lifetime of any data read.


                Creating new heap does not allocate any memory (except the memory necessary for  <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> structure itself). 
                The parameters <i>maxSize</i> and <i>trimSize</i> are used  as quotas onlyduring <a href="https://msdn.microsoft.com/633b6a11-09ba-48a7-a1ad-940846c65d79">WsAlloc</a> and <a href="https://msdn.microsoft.com/c927ccb9-66c8-4acf-bbb5-12313ea80ee0">WsResetHeap</a> operations.
            



