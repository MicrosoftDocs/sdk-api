---
UID: NF:rpcndr.NdrConformantStringBufferSize
title: NdrConformantStringBufferSize function (rpcndr.h)
description: The NdrConformantStringBufferSize function calculates the size of the buffer, in bytes, needed to marshal the conformant string.
helpviewer_keywords: ["NdrConformantStringBufferSize","NdrConformantStringBufferSize function [RPC]","rpc.ndrconformantstringbuffersize","rpcndr/NdrConformantStringBufferSize"]
old-location: rpc\ndrconformantstringbuffersize.htm
tech.root: Rpc
ms.assetid: 6090d96c-dd00-4df6-879b-893cd5b457b9
ms.date: 12/05/2018
ms.keywords: NdrConformantStringBufferSize, NdrConformantStringBufferSize function [RPC], rpc.ndrconformantstringbuffersize, rpcndr/NdrConformantStringBufferSize
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
 - NdrConformantStringBufferSize
 - rpcndr/NdrConformantStringBufferSize
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
 - NdrConformantStringBufferSize
---

# NdrConformantStringBufferSize function


## -description

The <b>NdrConformantStringBufferSize</b> function calculates the size of the buffer, in bytes, needed to marshal the conformant string.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the buffer. Structure is for internal use only; do not modify.

### -param pMemory [in]

Pointer to the null-terminated conformant string to be calculated.

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