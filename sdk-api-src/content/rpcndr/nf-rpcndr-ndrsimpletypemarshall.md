---
UID: NF:rpcndr.NdrSimpleTypeMarshall
title: NdrSimpleTypeMarshall function
author: windows-sdk-content
description: The NdrSimpleTypeMarshall function marshalls a simple type.
old-location: rpc\ndrsimpletypemarshall.htm
old-project: rpc
ms.assetid: af2bea36-d576-4144-8e21-3f89772465ed
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: NdrSimpleTypeMarshall, NdrSimpleTypeMarshall function [RPC], rpc.ndrsimpletypemarshall, rpcndr/NdrSimpleTypeMarshall
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrSimpleTypeMarshall
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: ADAM
---

# NdrSimpleTypeMarshall function


## -description


The <b>NdrSimpleTypeMarshall</b> function marshalls a simple type.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


### -param pMemory [in]

Pointer to the simple type to be marshalled.


### -param FormatChar [in]

Simple type format character.


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
 



