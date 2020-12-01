---
UID: NF:rpcndr.NdrSimpleStructUnmarshall
title: NdrSimpleStructUnmarshall function (rpcndr.h)
description: The NdrSimpleStructUnmarshall function unmarshals the simple structure from the network buffer to memory.
helpviewer_keywords: ["NdrSimpleStructUnmarshall","NdrSimpleStructUnmarshall function [Windows API]","rpcndr/NdrSimpleStructUnmarshall","winprog.ndrsimplestructunmarshall"]
old-location: winprog\ndrsimplestructunmarshall.htm
tech.root: winprog
ms.assetid: 6b4a28a3-3d0f-43c5-b59a-58c14435e28f
ms.date: 12/05/2018
ms.keywords: NdrSimpleStructUnmarshall, NdrSimpleStructUnmarshall function [Windows API], rpcndr/NdrSimpleStructUnmarshall, winprog.ndrsimplestructunmarshall
req.header: rpcndr.h
req.include-header: 
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
 - NdrSimpleStructUnmarshall
 - rpcndr/NdrSimpleStructUnmarshall
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
 - NdrSimpleStructUnmarshall
---

# NdrSimpleStructUnmarshall function


## -description

The <b>NdrSimpleStructUnmarshall</b> function unmarshals the simple structure from the network buffer to memory.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The  <b>MIDL_STUB_MESSAGE</b> structure is for internal use only, and must not be modified.

### -param ppMemory [out]

Address to a pointer to the unmarshalled simple structure. If set to null, or if the <i>fMustAlloc</i> parameter is set to <b>TRUE</b>, the stub will allocate the memory.

### -param pFormat [in]

Pointer to the format string description.

### -param fMustAlloc [in]

Flag that specifies whether the stub must allocate the memory into which the simple structure is to be marshaled.  Specify <b>TRUE</b> if RPC must allocate <i>ppMemory</i>.

## -returns

Returns null upon success. Raises one of the following exceptions upon failure.

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

## -see-also

<a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a>