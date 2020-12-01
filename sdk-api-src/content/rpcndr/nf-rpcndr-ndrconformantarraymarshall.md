---
UID: NF:rpcndr.NdrConformantArrayMarshall
title: NdrConformantArrayMarshall function (rpcndr.h)
description: The NdrConformantArrayMarshall function marshals the conformant array into a network buffer.
helpviewer_keywords: ["NdrComformantArrayMarshall","NdrConformantArrayMarshall","NdrConformantArrayMarshall function [Windows API]","rpcndr/NdrConformantArrayMarshall","winprog.ndrcomformantarraymarshall"]
old-location: winprog\ndrcomformantarraymarshall.htm
tech.root: winprog
ms.assetid: 28098531-a836-4a22-8c1a-fbf28d4a1bdd
ms.date: 12/05/2018
ms.keywords: NdrComformantArrayMarshall, NdrConformantArrayMarshall, NdrConformantArrayMarshall function [Windows API], rpcndr/NdrConformantArrayMarshall, winprog.ndrcomformantarraymarshall
req.header: rpcndr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - NdrConformantArrayMarshall
 - rpcndr/NdrConformantArrayMarshall
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
 - NdrConformantArrayMarshall
---

# NdrConformantArrayMarshall function


## -description

The <b>NdrConformantArrayMarshall</b> function marshals the conformant array into a network buffer.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The  <b>MIDL_STUB_MESSAGE</b> structure is for internal use only, and must not be modified.

### -param pMemory [in]

Pointer to the conformant array to be marshaled.

### -param pFormat [in]

Pointer to the format string description.

## -returns

Returns null upon success. Raises one of the following exceptions upon failure.

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

## -see-also

<a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a>