---
UID: NF:rpcndr.NdrPointerBufferSize
title: NdrPointerBufferSize function (rpcndr.h)
description: The NdrPointerBufferSize function computes the needed buffer size, in bytes, for a top-level pointer to anything.
helpviewer_keywords: ["NdrPointerBufferSize","NdrPointerBufferSize function [RPC]","rpc.ndrpointerbuffersize","rpcndr/NdrPointerBufferSize"]
old-location: rpc\ndrpointerbuffersize.htm
tech.root: Rpc
ms.assetid: fbab3c13-d696-430c-b3f5-7cb187678c33
ms.date: 12/05/2018
ms.keywords: NdrPointerBufferSize, NdrPointerBufferSize function [RPC], rpc.ndrpointerbuffersize, rpcndr/NdrPointerBufferSize
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
 - NdrPointerBufferSize
 - rpcndr/NdrPointerBufferSize
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
 - NdrPointerBufferSize
---

# NdrPointerBufferSize function


## -description

The <b>NdrPointerBufferSize</b> function computes the needed buffer size, in bytes, for a top-level pointer to anything.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the buffer. This structure is for internal use only and should not be modified.

### -param pMemory [in]

Pointer to the data being sized.

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

## -remarks

Pointers embedded in structures, arrays, or unions call 
    <b>NdrPointerBufferSize</b> directly. 

Used for FC_RP, FC_UP, FC_FP, FC_OP format strings.