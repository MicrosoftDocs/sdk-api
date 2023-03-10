---
UID: NF:rpcndr.NdrInterfacePointerUnmarshall
title: NdrInterfacePointerUnmarshall function (rpcndr.h)
description: The NdrInterfacePointerUnmarshall function unmarshalls the data referenced by the interface pointer from the network buffer to memory.
helpviewer_keywords: ["NdrInterfacePointerUnmarshall","NdrInterfacePointerUnmarshall function [RPC]","rpc.ndrinterfacepointerunmarshall","rpcndr/NdrInterfacePointerUnmarshall"]
old-location: rpc\ndrinterfacepointerunmarshall.htm
tech.root: Rpc
ms.assetid: b6ed9308-a935-44ed-a0e7-17d05d4762e5
ms.date: 12/05/2018
ms.keywords: NdrInterfacePointerUnmarshall, NdrInterfacePointerUnmarshall function [RPC], rpc.ndrinterfacepointerunmarshall, rpcndr/NdrInterfacePointerUnmarshall
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
 - NdrInterfacePointerUnmarshall
 - rpcndr/NdrInterfacePointerUnmarshall
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
 - NdrInterfacePointerUnmarshall
---

# NdrInterfacePointerUnmarshall function


## -description

The <b>NdrInterfacePointerUnmarshall</b> function unmarshalls the data referenced by the interface pointer from the network buffer to memory.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.

### -param ppMemory [out]

Pointer to a pointer to the unmarshalled interface pointer.

### -param pFormat [in]

Pointer to the format string description.

### -param fMustAlloc [in]

Unused.

## -returns

Returns NULL upon success. If an error occurs, the function throws one of the following exception codes. In addition, the function can throw exception codes from <a href="/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a>.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_BAD_STUB_DATA  </td>
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