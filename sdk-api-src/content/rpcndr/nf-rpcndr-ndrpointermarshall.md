---
UID: NF:rpcndr.NdrPointerMarshall
title: NdrPointerMarshall function
author: windows-sdk-content
description: The NdrPointerMarshall function marshalls a top level pointer to anything. Pointers embedded in structures, arrays, or unions call NdrPointerMarshall directly.
old-location: rpc\ndrpointermarshall.htm
old-project: Rpc
ms.assetid: efbdb93e-5d6b-4116-b1bf-8836cd9d7b89
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: NdrPointerMarshall, NdrPointerMarshall function [RPC], rpc.ndrpointermarshall, rpcndr/NdrPointerMarshall
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
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	RpcRT4.dll
api_name:
-	NdrPointerMarshall
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdrPointerMarshall function


## -description


The <b>NdrPointerMarshall</b> function marshalls a top level pointer to anything.  Pointers embedded in
    structures, arrays, or unions call <b>NdrPointerMarshall</b> directly.



## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


### -param pMemory [in]

Pointer to the pointer to be marshalled.


### -param pFormat [in]

Pointer to the format string description.


## -returns



Returns <b>NULL</b> upon success. If an error occurs, the function throws one of the following exception codes. 

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



This function is used for FC_RP, FC_UP, FC_FP, FC_OP format strings.



