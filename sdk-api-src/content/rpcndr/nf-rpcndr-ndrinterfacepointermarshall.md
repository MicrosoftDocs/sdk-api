---
UID: NF:rpcndr.NdrInterfacePointerMarshall
title: NdrInterfacePointerMarshall function (rpcndr.h)
description: The NdrInterfacePointerMarshall function marshals the interface pointer into a network buffer to be sent to the server.
helpviewer_keywords: ["NdrInterfacePointerMarshall","NdrInterfacePointerMarshall function [RPC]","rpc.ndrinterfacepointermarshall","rpcndr/NdrInterfacePointerMarshall"]
old-location: rpc\ndrinterfacepointermarshall.htm
tech.root: Rpc
ms.assetid: b6a8ca3c-a386-48c9-9347-ef9329678b5d
ms.date: 12/05/2018
ms.keywords: NdrInterfacePointerMarshall, NdrInterfacePointerMarshall function [RPC], rpc.ndrinterfacepointermarshall, rpcndr/NdrInterfacePointerMarshall
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
 - NdrInterfacePointerMarshall
 - rpcndr/NdrInterfacePointerMarshall
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
 - NdrInterfacePointerMarshall
---

# NdrInterfacePointerMarshall function


## -description

The <b>NdrInterfacePointerMarshall</b> function marshals the interface pointer into a network buffer to be sent to the server.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. This structure is for internal use only and should not be modified.

### -param pMemory [in]

Pointer to the interface pointer to be marshaled.

### -param pFormat [in]

Pointer to the format string description.

## -returns

Returns null upon success. If an error occurs, the function throws one of the following exception codes. In addition, the function can throw exception codes from <a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface">CoMarshalInterface</a>.

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