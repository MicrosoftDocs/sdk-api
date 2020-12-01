---
UID: NF:rpcndr.NdrComplexArrayMarshall
title: NdrComplexArrayMarshall function (rpcndr.h)
description: The NdrComplexArrayMarshall function marshals the complex array into a network buffer.
helpviewer_keywords: ["NdrComplexArrayMarshall","NdrComplexArrayMarshall function [Windows API]","rpcndr/NdrComplexArrayMarshall","winprog.ndrcomplexarraymarshall"]
old-location: winprog\ndrcomplexarraymarshall.htm
tech.root: winprog
ms.assetid: 01109e96-7d5b-4f16-a0fc-e7cf49020c3e
ms.date: 12/05/2018
ms.keywords: NdrComplexArrayMarshall, NdrComplexArrayMarshall function [Windows API], rpcndr/NdrComplexArrayMarshall, winprog.ndrcomplexarraymarshall
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
 - NdrComplexArrayMarshall
 - rpcndr/NdrComplexArrayMarshall
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
 - NdrComplexArrayMarshall
---

# NdrComplexArrayMarshall function


## -description

The <b>NdrComplexArrayMarshall</b> function marshals the complex array into a network buffer.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The  <b>MIDL_STUB_MESSAGE</b> structure is for internal use only, and must not be modified.

### -param pMemory [in]

Pointer to the complex array to be marshaled.

### -param pFormat [in]

Pointer to the format string description.

## -returns

Returns null upon success. Raises one of the following exceptions  upon failure.

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