---
UID: NF:rpcndr.NdrPointerUnmarshall
title: NdrPointerUnmarshall function
author: windows-sdk-content
description: The NdrPointerUnmarshall function unmarshalls a top level pointer to anything. Pointers embedded in structures, arrays, or unions call NdrPointerUnmarshall directly.
old-location: rpc\ndrpointerunmarshall.htm
old-project: rpc
ms.assetid: 6e4b0085-34bd-4f63-beea-a944ff0f853e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NdrPointerUnmarshall, NdrPointerUnmarshall function [RPC], rpc.ndrpointerunmarshall, rpcndr/NdrPointerUnmarshall
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
 - NdrPointerUnmarshall
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: ADAM
---

# NdrPointerUnmarshall function


## -description


The <b>NdrPointerUnmarshall</b> function unmarshalls a top level pointer to anything.  Pointers embedded in
    structures, arrays, or unions call <b>NdrPointerUnmarshall</b> directly.



## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


### -param ppMemory [in]

Pointer to memory where pointer will be unmarshalled. Please see MCCP Buffer Protection for information on buffer overrun protections in RPC: <a href="http://msdn.microsoft.com/en-us/library/ff621497(VS.85).aspx ">http://msdn.microsoft.com/en-us/library/ff621497(VS.85).aspx</a>


### -param pFormat [in]

Pointer to the format string description.


### -param fMustAlloc [in]

Unused.


## -returns



Returns <b>NULL</b> upon success. If an error occurs, the function throws one of the following exception codes.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_BAD_STUB_DATA or RPC_X_INVALID_BOUND  </td>
<td>The network  buffer is incorrect.</td>
</tr>
<tr>
<td>RPC_S_OUT_OF_MEMORY</td>
<td>The system is out of memory.</td>
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



This function is used for FC_RP, FC_UP, FC_FP, FC_OP format strings.




