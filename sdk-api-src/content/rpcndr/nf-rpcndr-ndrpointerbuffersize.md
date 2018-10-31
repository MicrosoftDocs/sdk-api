---
UID: NF:rpcndr.NdrPointerBufferSize
title: NdrPointerBufferSize function
author: windows-sdk-content
description: The NdrPointerBufferSize function computes the needed buffer size, in bytes, for a top-level pointer to anything.
old-location: rpc\ndrpointerbuffersize.htm
tech.root: rpc
ms.assetid: fbab3c13-d696-430c-b3f5-7cb187678c33
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: NdrPointerBufferSize, NdrPointerBufferSize function [RPC], rpc.ndrpointerbuffersize, rpcndr/NdrPointerBufferSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrPointerBufferSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdrPointerBufferSize function


## -description


The <b>NdrPointerBufferSize</b> function computes the needed buffer size, in bytes, for a top-level pointer to anything.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the buffer. This structure is for internal use only and should not be modified.


### -param pMemory [in]

Pointer to the data being sized.


### -param pFormat [in]

Pointer to the format string description.



## -returns



This function has no return values. If an error occurs, the function throws one of the following exception codes.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>STATUS_ACCESS_VIOLATION</td>
<td>An access violation occurred.</td>
</tr>
<tr>
<td>RPC_S_INTERNAL_ERROR</td>
<td>An error occurred in RPC.</td>
</tr>
</table>
 




## -remarks



Pointers embedded in structures, arrays, or unions call 
    <b>NdrPointerBufferSize</b> directly. 

Used for FC_RP, FC_UP, FC_FP, FC_OP format strings.




