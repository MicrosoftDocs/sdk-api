---
UID: NF:rpcndr.NdrInterfacePointerBufferSize
title: NdrInterfacePointerBufferSize function (rpcndr.h)
description: The NdrInterfacePointerBufferSize function calculates the size of the buffer, in bytes, needed to marshal the interface pointer.
helpviewer_keywords: ["NdrInterfacePointerBufferSize","NdrInterfacePointerBufferSize function [RPC]","rpc.ndrinterfacepointerbuffersize","rpcndr/NdrInterfacePointerBufferSize"]
old-location: rpc\ndrinterfacepointerbuffersize.htm
tech.root: Rpc
ms.assetid: 815ebf99-f616-44e3-9b87-25d9a889cf6b
ms.date: 12/05/2018
ms.keywords: NdrInterfacePointerBufferSize, NdrInterfacePointerBufferSize function [RPC], rpc.ndrinterfacepointerbuffersize, rpcndr/NdrInterfacePointerBufferSize
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NdrInterfacePointerBufferSize
 - rpcndr/NdrInterfacePointerBufferSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - NdrInterfacePointerBufferSize
---

# NdrInterfacePointerBufferSize function


## -description

The <b>NdrInterfacePointerBufferSize</b> function calculates the size of the buffer, in bytes, needed to marshal the interface pointer.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the buffer. This structure is for internal use only and should not be modified.

### -param pMemory [in]

Pointer to the interface pointer to be calculated.

### -param pFormat [in]

Pointer to the format string description.

## -returns

This function has no return values. If an error occurs, the function throws  one of the following exception codes. In addition, the function can throw exception codes from <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetmarshalsizemax">CoGetMarshalSizeMax</a>.

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