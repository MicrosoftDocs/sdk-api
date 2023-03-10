---
UID: NF:rpcndr.NdrConformantStringUnmarshall
title: NdrConformantStringUnmarshall function (rpcndr.h)
description: The NdrConformantStringUnmarshall function unmarshals the conformant string from the network buffer to memory.
helpviewer_keywords: ["NdrConformantStringUnmarshall","NdrConformantStringUnmarshall function [RPC]","rpc.ndrconformantstringunmarshall","rpcndr/NdrConformantStringUnmarshall"]
old-location: rpc\ndrconformantstringunmarshall.htm
tech.root: Rpc
ms.assetid: 3965e5aa-8695-4dd3-a75b-ee007ee3cccd
ms.date: 12/05/2018
ms.keywords: NdrConformantStringUnmarshall, NdrConformantStringUnmarshall function [RPC], rpc.ndrconformantstringunmarshall, rpcndr/NdrConformantStringUnmarshall
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
 - NdrConformantStringUnmarshall
 - rpcndr/NdrConformantStringUnmarshall
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
 - NdrConformantStringUnmarshall
---

# NdrConformantStringUnmarshall function


## -description

The <b>NdrConformantStringUnmarshall</b> function unmarshals the conformant string from the network buffer to memory.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. This structure is for internal use only and should not be modified.

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