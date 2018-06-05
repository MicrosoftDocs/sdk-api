---
UID: NF:rpcndr.NdrOleAllocate
title: NdrOleAllocate function
author: windows-sdk-content
description: The NdrOleAllocate function is used by RPC to allocate memory for an object interface. This function is a wrapper for the CoTaskMemAlloc function.
old-location: rpc\ndroleallocate.htm
old-project: Rpc
ms.assetid: 87bfc8ae-62e6-477f-98a7-caf907589b89
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: NdrOleAllocate, NdrOleAllocate function [RPC], rpc.ndroleallocate, rpcndr/NdrOleAllocate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	RpcRT4.dll
api_name:
-	NdrOleAllocate
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdrOleAllocate function


## -description


The <b>NdrOleAllocate</b> function is used by RPC to allocate memory for an object interface. This function is a wrapper for the <a href="_com_cotaskmemalloc">CoTaskMemAlloc</a> function.


## -parameters




### -param Size

TBD




#### - size [in]

Memory to allocate, in bytes.


## -returns



Returns a void pointer to the allocated space upon success. Returns null upon failure due to insufficient memory.




## -remarks



To return a pointer other than a void, use a type cast on the return value. The memory pointed to by the return value is guaranteed to be suitably aligned for the storage of any type of object. If the <i>Size</i> parameter is zero, <b>NdrOleAllocate</b> allocates a zero-length item in the heap and returns a valid pointer to that item. Always check the return value from <b>NdrOleAllocate</b>, even if the amount of memory requested is small.




## -see-also




<a href="_com_cotaskmemalloc">CoTaskMemAlloc</a>
 

 

