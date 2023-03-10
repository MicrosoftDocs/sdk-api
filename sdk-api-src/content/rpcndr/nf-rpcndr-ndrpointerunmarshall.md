---
UID: NF:rpcndr.NdrPointerUnmarshall
title: NdrPointerUnmarshall function (rpcndr.h)
description: The NdrPointerUnmarshall function unmarshalls a top level pointer to anything. Pointers embedded in structures, arrays, or unions call NdrPointerUnmarshall directly.
helpviewer_keywords: ["NdrPointerUnmarshall","NdrPointerUnmarshall function [RPC]","rpc.ndrpointerunmarshall","rpcndr/NdrPointerUnmarshall"]
old-location: rpc\ndrpointerunmarshall.htm
tech.root: Rpc
ms.assetid: 6e4b0085-34bd-4f63-beea-a944ff0f853e
ms.date: 12/05/2018
ms.keywords: NdrPointerUnmarshall, NdrPointerUnmarshall function [RPC], rpc.ndrpointerunmarshall, rpcndr/NdrPointerUnmarshall
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
 - NdrPointerUnmarshall
 - rpcndr/NdrPointerUnmarshall
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
 - NdrPointerUnmarshall
---

# NdrPointerUnmarshall function


## -description

The <b>NdrPointerUnmarshall</b> function unmarshalls a top level pointer to anything.  Pointers embedded in
    structures, arrays, or unions call <b>NdrPointerUnmarshall</b> directly.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.

### -param ppMemory [in]

Pointer to memory where pointer will be unmarshalled. Please see MCCP Buffer Protection for information on buffer overrun protections in RPC: <a href="/windows/desktop/Rpc/mccp-buffer-protection">http://msdn.microsoft.com/en-us/library/ff621497(VS.85).aspx</a>

### -param pFormat [in]

Pointer to the format string description.

### -param fMustAlloc [in]

Unused.

## -returns

Returns <b>NULL</b> upon success. If an error occurs, the function throws one of the following exception codes.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_BAD_STUB_DATA or RPC_X_INVALID_BOUND  </td>
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

## -remarks

This function is used for FC_RP, FC_UP, FC_FP, FC_OP format strings.