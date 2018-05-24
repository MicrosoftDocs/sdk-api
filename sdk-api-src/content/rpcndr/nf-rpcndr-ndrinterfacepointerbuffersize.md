---
UID: NF:rpcndr.NdrInterfacePointerBufferSize
title: NdrInterfacePointerBufferSize function
author: windows-driver-content
description: The NdrInterfacePointerBufferSize function calculates the size of the buffer, in bytes, needed to marshal the interface pointer.
old-location: rpc\ndrinterfacepointerbuffersize.htm
old-project: Rpc
ms.assetid: 815ebf99-f616-44e3-9b87-25d9a889cf6b
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: NdrInterfacePointerBufferSize, NdrInterfacePointerBufferSize function [RPC], rpc.ndrinterfacepointerbuffersize, rpcndr/NdrInterfacePointerBufferSize
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	NdrInterfacePointerBufferSize
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdrInterfacePointerBufferSize function


## -description


The <b>NdrInterfacePointerBufferSize</b> function calculates the size of the buffer, in bytes, needed to marshal the interface pointer.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the buffer. This structure is for internal use only and should not be modified.


### -param pMemory [in]

Pointer to the interface pointer to be calculated.


### -param pFormat [in]

Pointer to the format string description.


## -returns



This function has no return values. If an error occurs, the function throws  one of the following exception codes. In addition, the function can throw exception codes from <a href="_com_cogetmarshalsizemax">CoGetMarshalSizeMax</a>.

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
 



