---
UID: NF:rpcndr.NdrUserMarshalMarshall
title: NdrUserMarshalMarshall function (rpcndr.h)
description: The NdrUserMarshalMarshall function marshals the supplied data buffer.
helpviewer_keywords: ["NdrUserMarshalMarshall","NdrUserMarshalMarshall function [RPC]","rpc.ndrusermarshalmarshall","rpcndr/NdrUserMarshalMarshall"]
old-location: rpc\ndrusermarshalmarshall.htm
tech.root: Rpc
ms.assetid: 9c89f342-2356-4a58-81bf-f9e53535468e
ms.date: 12/05/2018
ms.keywords: NdrUserMarshalMarshall, NdrUserMarshalMarshall function [RPC], rpc.ndrusermarshalmarshall, rpcndr/NdrUserMarshalMarshall
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
 - NdrUserMarshalMarshall
 - rpcndr/NdrUserMarshalMarshall
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
 - NdrUserMarshalMarshall
---

# NdrUserMarshalMarshall function


## -description

The <b>NdrUserMarshalMarshall</b> function marshals the supplied data buffer.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.

### -param pMemory [in]

Pointer to user data object to be marshaled.

### -param pFormat [in]

Pointer's format string description.

## -returns

Returns <b>NULL</b> upon success. If an error occurs, the function throws one of the following exception codes. 

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