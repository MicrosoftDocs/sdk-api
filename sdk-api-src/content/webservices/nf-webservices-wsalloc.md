---
UID: NF:webservices.WsAlloc
title: WsAlloc function
author: windows-sdk-content
description: Allocates a segment of memory from the specified heap.
old-location: wsw\wsalloc.htm
old-project: wsw
ms.assetid: 633b6a11-09ba-48a7-a1ad-940846c65d79
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WsAlloc, WsAlloc function [Web Services for Windows], webservices/WsAlloc, wsw.wsalloc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsAlloc
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsAlloc function


## -description



Allocates a segment of memory from the specified <a href="https://msdn.microsoft.com/3a25284a-8f15-42d4-a292-ece28a08fb69">heap</a>. 




## -parameters




### -param heap [in]

Pointer to a <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> structure representing the heap from which to allocate the memory.
                


### -param size [in]

The number of bytes to allocate.  This value can be zero.
                


### -param ptr

On success, a pointer that receives the address of the allocated memory. This pointer is valid until <a href="https://msdn.microsoft.com/ec643915-8c4b-4916-b390-d6ca043350db">WsFreeHeap</a> or <a href="https://msdn.microsoft.com/c927ccb9-66c8-4acf-bbb5-12313ea80ee0">WsResetHeap</a> is called on the <a href="https://msdn.microsoft.com/3a25284a-8f15-42d4-a292-ece28a08fb69">heap</a>. 



The returned pointer is aligned on an 8-byte boundary. 



Zero byte allocations will return a non-NULL pointer. 




### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                


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
The requested bytes, in addition to already allocated bytes, exceed the size of the <a href="https://msdn.microsoft.com/3a25284a-8f15-42d4-a292-ece28a08fb69">heap</a>, as specified by the <a href="https://msdn.microsoft.com/c047a3b9-27a1-464c-b9f9-0b0c6cf8eb97">WS_HEAP_PROPERTY_MAX_SIZE</a> property.  
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficent memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



The memory returned by this function is not zero initialized and contains undefined values.
                



