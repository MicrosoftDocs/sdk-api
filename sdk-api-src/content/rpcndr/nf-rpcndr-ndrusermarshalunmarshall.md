---
UID: NF:rpcndr.NdrUserMarshalUnmarshall
title: NdrUserMarshalUnmarshall function (rpcndr.h)
description: The NdrUserMarshalUnmarshall function calls a user-defined unmarshal routine to unmarshal data with the attribute.
helpviewer_keywords: ["NdrUserMarshalUnmarshall","NdrUserMarshalUnmarshall function [Windows API]","rpcndr/NdrUserMarshalUnmarshall","winprog.ndrusermarshalunmarshall"]
old-location: winprog\ndrusermarshalunmarshall.htm
tech.root: winprog
ms.assetid: 8012973b-a41f-4729-a04a-8a1afb29cebe
ms.date: 12/05/2018
ms.keywords: NdrUserMarshalUnmarshall, NdrUserMarshalUnmarshall function [Windows API], rpcndr/NdrUserMarshalUnmarshall, winprog.ndrusermarshalunmarshall
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
 - NdrUserMarshalUnmarshall
 - rpcndr/NdrUserMarshalUnmarshall
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
 - NdrUserMarshalUnmarshall
---

# NdrUserMarshalUnmarshall function


## -description

The <b>NdrUserMarshalUnmarshall</b> function calls a user-defined unmarshal routine to unmarshal data with the  attribute.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The  <b>MIDL_STUB_MESSAGE</b> structure is for internal use only, and must not be modified.

### -param ppMemory [in]

Pointer to user data object to be unmarshalled.

### -param pFormat [in]

Format string description of the pointer.

### -param fMustAlloc [in]

Flag that specifies whether the stub must allocate the memory into which the user data object is to be unmarshalled.  Specify <b>TRUE</b> if RPC must allocate <i>ppMemory</i>.

## -returns

Returns <b>NULL</b> upon success. Returns one of the following exception codes upon error.

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



<a href="https://msdn.microsoft.com/">wire_marshal</a>