---
UID: NF:rpcndr.NdrConformantStringMarshall
title: NdrConformantStringMarshall function
author: windows-sdk-content
description: The NdrConformantStringMarshall function marshals the conformant string into a network buffer to be sent to the server.
old-location: rpc\ndrconformantstringmarshall.htm
tech.root: Rpc
ms.assetid: d2e323fb-2bb2-4c6c-8f26-fc7e19c7fea7
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: NdrConformantStringMarshall, NdrConformantStringMarshall function [RPC], rpc.ndrconformantstringmarshall, rpcndr/NdrConformantStringMarshall
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
 - NdrConformantStringMarshall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdrConformantStringMarshall function


## -description


The <b>NdrConformantStringMarshall</b> function marshals the conformant string into a network buffer to be sent to the server.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. This structure is for internal use only and should not be modified.


### -param pMemory [in]

Pointer to the null-terminated conformant string to be marshaled.


### -param pFormat [in]

Pointer to the format string description.


## -returns



Returns null upon success. If an error occurs, the function throws one of the following exception codes.

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
 



