---
UID: NF:rpcndr.NdrUserMarshalMarshall
title: NdrUserMarshalMarshall function
author: windows-sdk-content
description: The NdrUserMarshalMarshall function marshals the supplied data buffer.
old-location: rpc\ndrusermarshalmarshall.htm
tech.root: Rpc
ms.assetid: 9c89f342-2356-4a58-81bf-f9e53535468e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: NdrUserMarshalMarshall, NdrUserMarshalMarshall function [RPC], rpc.ndrusermarshalmarshall, rpcndr/NdrUserMarshalMarshall
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
 - NdrUserMarshalMarshall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdrUserMarshalMarshall function


## -description


The <b>NdrUserMarshalMarshall</b> function marshals the supplied data buffer.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


### -param pMemory [in]

Pointer to user data object to be marshaled.


### -param pFormat [in]

Pointer's format string description.


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
 



