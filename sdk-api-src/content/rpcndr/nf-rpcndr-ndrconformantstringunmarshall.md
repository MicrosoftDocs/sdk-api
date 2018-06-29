---
UID: NF:rpcndr.NdrConformantStringUnmarshall
title: NdrConformantStringUnmarshall function
author: windows-sdk-content
description: The NdrConformantStringUnmarshall function unmarshals the conformant string from the network buffer to memory.
old-location: rpc\ndrconformantstringunmarshall.htm
old-project: Rpc
ms.assetid: 3965e5aa-8695-4dd3-a75b-ee007ee3cccd
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: NdrConformantStringUnmarshall, NdrConformantStringUnmarshall function [RPC], rpc.ndrconformantstringunmarshall, rpcndr/NdrConformantStringUnmarshall
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrConformantStringUnmarshall
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: ADAM
---

# NdrConformantStringUnmarshall function


## -description


The <b>NdrConformantStringUnmarshall</b> function unmarshals the conformant string from the network buffer to memory.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. This structure is for internal use only and should not be modified.  


### -param ppMemory [out]

Address to a pointer to the unmarshalled conformant string. If set to null, or if the <i>fMustAlloc</i> is set to <b>TRUE</b>, the stub will allocate the memory.


### -param pFormat [in]

Pointer to the format string description.


### -param fMustAlloc [in]

Flag that specifies whether the stub must allocate the memory into which the conformant string is to be marshaled.  Specify <b>TRUE</b> if RPC must allocate <i>ppMemory</i>. 


## -returns



Returns null upon success. If an error occurs, the function throws one of the following exception codes.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_BAD_STUB_DATA or RPC_X_INVALID_BOUND</td>
<td>The network  is incorrect.</td>
</tr>
<tr>
<td>RPC_S_OUT_OF_MEMORY</td>
<td>Out of memory.</td>
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
 



