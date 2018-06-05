---
UID: NF:rpcndr.NdrInterfacePointerUnmarshall
title: NdrInterfacePointerUnmarshall function
author: windows-sdk-content
description: The NdrInterfacePointerUnmarshall function unmarshalls the data referenced by the interface pointer from the network buffer to memory.
old-location: rpc\ndrinterfacepointerunmarshall.htm
old-project: Rpc
ms.assetid: b6ed9308-a935-44ed-a0e7-17d05d4762e5
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: NdrInterfacePointerUnmarshall, NdrInterfacePointerUnmarshall function [RPC], rpc.ndrinterfacepointerunmarshall, rpcndr/NdrInterfacePointerUnmarshall
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
-	NdrInterfacePointerUnmarshall
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdrInterfacePointerUnmarshall function


## -description


The <b>NdrInterfacePointerUnmarshall</b> function unmarshalls the data referenced by the interface pointer from the network buffer to memory.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


### -param ppMemory [out]

Pointer to a pointer to the unmarshalled interface pointer. 


### -param pFormat [in]

Pointer to the format string description.


### -param fMustAlloc [in]

Unused.


## -returns



Returns NULL upon success. If an error occurs, the function throws one of the following exception codes. In addition, the function can throw exception codes from <a href="_com_counmarshalinterface">CoUnmarshalInterface</a>.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_BAD_STUB_DATA  </td>
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
 



