---
UID: NF:rpcndr.NdrConformantStringMarshall
title: NdrConformantStringMarshall function (rpcndr.h)
description: The NdrConformantStringMarshall function marshals the conformant string into a network buffer to be sent to the server.
helpviewer_keywords: ["NdrConformantStringMarshall","NdrConformantStringMarshall function [RPC]","rpc.ndrconformantstringmarshall","rpcndr/NdrConformantStringMarshall"]
old-location: rpc\ndrconformantstringmarshall.htm
tech.root: Rpc
ms.assetid: d2e323fb-2bb2-4c6c-8f26-fc7e19c7fea7
ms.date: 12/05/2018
ms.keywords: NdrConformantStringMarshall, NdrConformantStringMarshall function [RPC], rpc.ndrconformantstringmarshall, rpcndr/NdrConformantStringMarshall
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
 - NdrConformantStringMarshall
 - rpcndr/NdrConformantStringMarshall
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
 - NdrConformantStringMarshall
---

# NdrConformantStringMarshall function


## -description

The <b>NdrConformantStringMarshall</b> function marshals the conformant string into a network buffer to be sent to the server.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. This structure is for internal use only and should not be modified.

### -param pMemory [in]

Pointer to the null-terminated conformant string to be marshaled.

### -param pFormat [in]

Pointer to the format string description.

## -returns

Returns null upon success. If an error occurs, the function throws one of the following exception codes.

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