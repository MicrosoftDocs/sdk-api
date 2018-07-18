---
UID: NF:rpcndr.NdrInterfacePointerMarshall
title: NdrInterfacePointerMarshall function
author: windows-sdk-content
description: The NdrInterfacePointerMarshall function marshals the interface pointer into a network buffer to be sent to the server.
old-location: rpc\ndrinterfacepointermarshall.htm
old-project: rpc
ms.assetid: b6a8ca3c-a386-48c9-9347-ef9329678b5d
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: NdrInterfacePointerMarshall, NdrInterfacePointerMarshall function [RPC], rpc.ndrinterfacepointermarshall, rpcndr/NdrInterfacePointerMarshall
ms.prod: windows
ms.technology: windows-sdk
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
 - NdrInterfacePointerMarshall
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: ADAM
---

# NdrInterfacePointerMarshall function


## -description


The <b>NdrInterfacePointerMarshall</b> function marshals the interface pointer into a network buffer to be sent to the server.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. This structure is for internal use only and should not be modified.


### -param pMemory [in]

Pointer to the interface pointer to be marshaled.


### -param pFormat [in]

Pointer to the format string description.


## -returns



Returns null upon success. If an error occurs, the function throws one of the following exception codes. In addition, the function can throw exception codes from <a href="https://msdn.microsoft.com/library/ms678428(v=VS.85).aspx">CoMarshalInterface</a>.

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
 



