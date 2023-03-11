---
UID: NF:rpcndr.NdrSimpleTypeUnmarshall
title: NdrSimpleTypeUnmarshall function (rpcndr.h)
description: The NdrSimpleTypeUnmarshall function unmarshalls a simple type.
helpviewer_keywords: ["NdrSimpleTypeUnmarshall","NdrSimpleTypeUnmarshall function [RPC]","rpc.ndrsimpletypeunmarshall","rpcndr/NdrSimpleTypeUnmarshall"]
old-location: rpc\ndrsimpletypeunmarshall.htm
tech.root: Rpc
ms.assetid: f1ed9bdc-3ff6-4947-b77f-cb95fe8c3e85
ms.date: 12/05/2018
ms.keywords: NdrSimpleTypeUnmarshall, NdrSimpleTypeUnmarshall function [RPC], rpc.ndrsimpletypeunmarshall, rpcndr/NdrSimpleTypeUnmarshall
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
 - NdrSimpleTypeUnmarshall
 - rpcndr/NdrSimpleTypeUnmarshall
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
 - NdrSimpleTypeUnmarshall
---

# NdrSimpleTypeUnmarshall function


## -description

The <b>NdrSimpleTypeUnmarshall</b> function unmarshalls a simple type.

## -parameters

### -param pStubMsg [in, out]

Pointer to a <a href="/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.

### -param pMemory [in]

Pointer to memory to unmarshall.

### -param FormatChar [in]

Format string of the simple type.

## -returns

 If an error occurs, the function throws one of the following exception codes. 

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