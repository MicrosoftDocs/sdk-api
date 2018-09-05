---
UID: NF:rpcndr.NdrConformantStringBufferSize
title: NdrConformantStringBufferSize function
author: windows-sdk-content
description: The NdrConformantStringBufferSize function calculates the size of the buffer, in bytes, needed to marshal the conformant string.
old-location: rpc\ndrconformantstringbuffersize.htm
old-project: Rpc
ms.assetid: 6090d96c-dd00-4df6-879b-893cd5b457b9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: NdrConformantStringBufferSize, NdrConformantStringBufferSize function [RPC], rpc.ndrconformantstringbuffersize, rpcndr/NdrConformantStringBufferSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.redist: 
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
tech.root: 
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrConformantStringBufferSize
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: ADAM
---

# NdrConformantStringBufferSize function


## -description


The <b>NdrConformantStringBufferSize</b> function calculates the size of the buffer, in bytes, needed to marshal the conformant string.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the buffer. Structure is for internal use only; do not modify. 


### -param pMemory [in]

Pointer to the null-terminated conformant string to be calculated.


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
 



