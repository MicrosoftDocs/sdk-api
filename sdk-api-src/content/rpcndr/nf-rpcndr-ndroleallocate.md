---
UID: NF:rpcndr.NdrOleAllocate
title: NdrOleAllocate function (rpcndr.h)
description: The NdrOleAllocate function is used by RPC to allocate memory for an object interface. This function is a wrapper for the CoTaskMemAlloc function.
helpviewer_keywords: ["NdrOleAllocate","NdrOleAllocate function [RPC]","rpc.ndroleallocate","rpcndr/NdrOleAllocate"]
old-location: rpc\ndroleallocate.htm
tech.root: Rpc
ms.assetid: 87bfc8ae-62e6-477f-98a7-caf907589b89
ms.date: 12/05/2018
ms.keywords: NdrOleAllocate, NdrOleAllocate function [RPC], rpc.ndroleallocate, rpcndr/NdrOleAllocate
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NdrOleAllocate
 - rpcndr/NdrOleAllocate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - NdrOleAllocate
---

# NdrOleAllocate function


## -description

The <b>NdrOleAllocate</b> function is used by RPC to allocate memory for an object interface. This function is a wrapper for the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> function.

## -parameters

### -param Size [in]

Memory to allocate, in bytes.

## -returns

Returns a void pointer to the allocated space upon success. Returns null upon failure due to insufficient memory.

## -remarks

To return a pointer other than a void, use a type cast on the return value. The memory pointed to by the return value is guaranteed to be suitably aligned for the storage of any type of object. If the <i>Size</i> parameter is zero, <b>NdrOleAllocate</b> allocates a zero-length item in the heap and returns a valid pointer to that item. Always check the return value from <b>NdrOleAllocate</b>, even if the amount of memory requested is small.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>